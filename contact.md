---
layout: page
title: Contact Us
permalink: /contact/
---

<div class="max-w-3xl mx-auto py-12 px-4 sm:px-6 lg:px-8" 
     x-data="{
        formData: {
            name: '',
            email: '',
            recipient: 'General Inquiry',
            message: '',
            bot_check: '' // Honeypot field
        },
        loading: false,
        success: false,
        error: false,
        errorMessage: 'Something went wrong. Please try again.',
        
        get isFormValid() {
            return this.formData.name.trim() !== '' && 
                   this.formData.email.trim() !== '' && 
                   this.formData.message.trim() !== '';
        },

        async submitForm() {
            // honeypot check
            if (this.formData.bot_check !== '') {
                // If the bot field is filled, pretend success but do nothing.
                this.success = true;
                return;
            }

            this.loading = true;
            this.error = false;

            // Prepare payload
            const payload = {
                name: this.formData.name,
                email: this.formData.email,
                recipient: this.formData.recipient, // Used by n8n to route
                message: this.formData.message
            };

            // TODO: Replace with actual n8n webhook URL when ready
            // For now, simulate a network request
            try {
                // Simulate delay
                await new Promise(resolve => setTimeout(resolve, 1000));
                
                // Simulate success (Uncomment fetch below when URL is ready)
                /*
                const response = await fetch('YOUR_N8N_WEBHOOK_URL', {
                    method: 'POST',
                    headers: { 'Content-Type': 'application/json' },
                    body: JSON.stringify(payload)
                });
                if (!response.ok) throw new Error('Network error');
                */
                
                this.success = true;
                this.formData.name = '';
                this.formData.email = '';
                this.formData.message = '';
                this.formData.recipient = 'General Inquiry';
                
            } catch (e) {
                this.error = true;
                console.error(e);
            } finally {
                this.loading = false;
            }
        }
     }">

    <div class="text-center mb-12">
        <p class="mt-4 text-lg leading-6 text-gray-500 dark:text-gray-300">
            Have a question? Use the form below to get in touch with the right team.
        </p>
    </div>

    <div class="bg-white dark:bg-gray-800 shadow overflow-hidden sm:rounded-lg">
        <div class="px-4 py-5 sm:p-6">
            
            <!-- Success Message -->
            <div x-show="success" x-transition class="mb-6 bg-green-50 border-l-4 border-green-400 p-4">
                <div class="flex">
                    <div class="flex-shrink-0">
                        <svg class="h-5 w-5 text-green-400" fill="currentColor" viewBox="0 0 20 20">
                            <path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z" clip-rule="evenodd"/>
                        </svg>
                    </div>
                    <div class="ml-3">
                        <p class="text-sm text-green-700">
                            Message sent successfully! We'll get back to you shortly.
                        </p>
                    </div>
                </div>
            </div>

             <!-- Error Message -->
            <div x-show="error" x-transition class="mb-6 bg-red-50 border-l-4 border-red-400 p-4">
                <div class="flex">
                    <div class="flex-shrink-0">
                        <svg class="h-5 w-5 text-red-400" fill="currentColor" viewBox="0 0 20 20">
                            <path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zM8.707 7.293a1 1 0 00-1.414 1.414L8.586 10l-1.293 1.293a1 1 0 101.414 1.414L10 11.414l1.293 1.293a1 1 0 001.414-1.414L11.414 10l1.293-1.293a1 1 0 00-1.414-1.414L10 8.586 8.707 7.293z" clip-rule="evenodd"/>
                        </svg>
                    </div>
                    <div class="ml-3">
                        <p class="text-sm text-red-700" x-text="errorMessage"></p>
                    </div>
                </div>
            </div>

            <form @submit.prevent="submitForm" class="grid grid-cols-1 gap-y-6 sm:grid-cols-2 sm:gap-x-8">
                
                <!-- Recipient Dropdown -->
                <div class="sm:col-span-2">
                    <label for="recipient" class="block text-sm font-medium text-gray-700 dark:text-gray-300">Who do you want to contact?</label>
                    <div class="mt-1">
                        <select id="recipient" name="recipient" x-model="formData.recipient" class="py-3 px-4 block w-full shadow-sm focus:ring-brand-500 focus:border-brand-500 border-gray-300 dark:border-gray-600 dark:bg-gray-700 dark:text-white rounded-md">
                            <option>General Inquiry</option>
                            <option>Officers</option>
                            <option>ARES</option>
                            <option>Media Inquiry</option>
                            <option>Community Support</option>
                        </select>
                    </div>
                </div>

                <!-- Name -->
                <div class="sm:col-span-2">
                    <label for="name" class="block text-sm font-medium text-gray-700 dark:text-gray-300">Name</label>
                    <div class="mt-1">
                        <input type="text" name="name" id="name" autocomplete="given-name" x-model="formData.name" required
                            class="py-3 px-4 block w-full shadow-sm focus:ring-brand-500 focus:border-brand-500 border-gray-300 dark:border-gray-600 dark:bg-gray-700 dark:text-white rounded-md">
                    </div>
                </div>

                <!-- Email -->
                <div class="sm:col-span-2">
                    <label for="email" class="block text-sm font-medium text-gray-700 dark:text-gray-300">Email</label>
                    <div class="mt-1">
                        <input id="email" name="email" type="email" autocomplete="email" x-model="formData.email" required 
                            class="py-3 px-4 block w-full shadow-sm focus:ring-brand-500 focus:border-brand-500 border-gray-300 dark:border-gray-600 dark:bg-gray-700 dark:text-white rounded-md">
                    </div>
                </div>

                <!-- Message -->
                <div class="sm:col-span-2">
                    <label for="message" class="block text-sm font-medium text-gray-700 dark:text-gray-300">Message</label>
                    <div class="mt-1">
                        <textarea id="message" name="message" rows="4" x-model="formData.message" required 
                            class="py-3 px-4 block w-full shadow-sm focus:ring-brand-500 focus:border-brand-500 border border-gray-300 dark:border-gray-600 dark:bg-gray-700 dark:text-white rounded-md"></textarea>
                    </div>
                </div>

                <!-- Honeypot (Hidden) -->
                <div class="hidden" aria-hidden="true">
                    <label for="bot_check">Don't fill this out if you're human:</label>
                    <input type="text" name="bot_check" id="bot_check" x-model="formData.bot_check" tabindex="-1">
                </div>

                <!-- Submit Button -->
                <div class="sm:col-span-2">
                    <button type="submit" 
                            :disabled="loading || !isFormValid"
                            :class="{ 'opacity-50 cursor-not-allowed': loading || !isFormValid, 'hover:bg-brand-900': !loading && isFormValid }"
                            class="w-full inline-flex items-center justify-center px-6 py-3 border border-transparent rounded-md shadow-sm text-base font-medium text-white bg-brand-800 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-brand-500 transition-colors">
                        <span x-show="loading" class="mr-2">
                            <svg class="animate-spin h-5 w-5 text-white" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24">
                                <circle class="opacity-25" cx="12" cy="12" r="10" stroke="currentColor" stroke-width="4"></circle>
                                <path class="opacity-75" fill="currentColor" d="M4 12a8 8 0 018-8V0C5.373 0 0 5.373 0 12h4zm2 5.291A7.962 7.962 0 014 12H0c0 3.042 1.135 5.824 3 7.938l3-2.647z"></path>
                            </svg>
                        </span>
                        <span x-text="loading ? 'Sending...' : 'Send Message'"></span>
                    </button>
                </div>
            </form>
        </div>
    </div>
</div>
