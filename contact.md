---
layout: default
title: Contact Us
permalink: /contact/
---

<div class="bg-white dark:bg-gray-800 shadow overflow-hidden sm:rounded-lg">
  <div class="px-4 py-5 sm:px-6">
    <h1 class="text-2xl leading-6 font-medium text-gray-900 dark:text-white">Contact Us</h1>
    <p class="mt-1 max-w-2xl text-sm text-gray-500 dark:text-gray-300">
      If you have any questions or would like more information about the club, please feel free to contact us.
    </p>
  </div>
  
  <div class="border-t border-gray-200 dark:border-gray-700 px-4 py-5 sm:p-0">
    <dl class="sm:divide-y sm:divide-gray-200 dark:sm:divide-gray-700">
      <div class="py-4 sm:py-5 sm:grid sm:grid-cols-3 sm:gap-4 sm:px-6">
        <dt class="text-sm font-medium text-gray-500 dark:text-gray-400">Email address</dt>
        <dd class="mt-1 text-sm text-gray-900 dark:text-white sm:mt-0 sm:col-span-2">
          <a href="mailto:k0ety@arrl.net" class="text-brand-800 hover:text-brand-900">k0ety@arrl.net</a>
        </dd>
      </div>
    </dl>
  </div>
</div>

<div class="mt-8 bg-white dark:bg-gray-800 shadow sm:rounded-lg">
  <div class="px-4 py-5 sm:p-6">
    <h3 class="text-lg leading-6 font-medium text-gray-900 dark:text-white">Send us a message</h3>
    <div class="mt-5 max-w-xl text-sm text-gray-500 dark:text-gray-300">
      <p>Fill out the form below and we will get back to you as soon as possible.</p>
    </div>
    <form action="#" method="POST" class="mt-6 grid grid-cols-1 gap-y-6 sm:grid-cols-2 sm:gap-x-8">
      <div class="sm:col-span-2">
        <label for="name" class="block text-sm font-medium text-gray-700 dark:text-gray-300">Name</label>
        <div class="mt-1">
          <input type="text" name="name" id="name" autocomplete="name" class="py-3 px-4 block w-full shadow-sm focus:ring-brand-800 focus:border-brand-800 border-gray-300 rounded-md dark:bg-gray-700 dark:border-gray-600 dark:text-white">
        </div>
      </div>
      <div class="sm:col-span-2">
        <label for="email" class="block text-sm font-medium text-gray-700 dark:text-gray-300">Email</label>
        <div class="mt-1">
          <input type="email" name="email" id="email" autocomplete="email" class="py-3 px-4 block w-full shadow-sm focus:ring-brand-800 focus:border-brand-800 border-gray-300 rounded-md dark:bg-gray-700 dark:border-gray-600 dark:text-white">
        </div>
      </div>
      <div class="sm:col-span-2">
        <label for="message" class="block text-sm font-medium text-gray-700 dark:text-gray-300">Message</label>
        <div class="mt-1">
          <textarea id="message" name="message" rows="4" class="py-3 px-4 block w-full shadow-sm focus:ring-brand-800 focus:border-brand-800 border-gray-300 rounded-md dark:bg-gray-700 dark:border-gray-600 dark:text-white"></textarea>
        </div>
      </div>
      <div class="sm:col-span-2">
        <button type="submit" class="w-full inline-flex items-center justify-center px-6 py-3 border border-transparent rounded-md shadow-sm text-base font-medium text-white bg-brand-800 hover:bg-brand-900 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-brand-800">
          Send Message
        </button>
      </div>
    </form>
  </div>
</div>
