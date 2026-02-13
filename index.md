---
layout: default
title: Home
---

<!-- Row 1: Hero (2/3) and Next Event (1/3) -->
<div class="grid grid-cols-1 lg:grid-cols-3 gap-6 mb-6">
    <!-- Hero Card -->
    <div class="lg:col-span-2 bg-white dark:bg-gray-800 shadow rounded-lg overflow-hidden flex flex-col justify-center p-8 relative">
        <div class="absolute inset-0 opacity-10 dark:opacity-20 pointer-events-none">
             <!-- Optional: Add a subtle background pattern or image here -->
             <img src="{{ '/assets/images/mmarc.jpg' | relative_url }}" class="w-full h-full object-cover grayscale" alt="Background">
        </div>
        <div class="relative z-10">
            <h1 class="text-4xl font-extrabold text-gray-900 dark:text-white sm:text-5xl mb-4">
                Mid-MO Amateur Radio Club
            </h1>
            <p class="text-xl text-gray-600 dark:text-gray-300 mb-6">
                Serving Jefferson City and Central Missouri (K0ETY). We are a community of radio enthusiasts dedicated to emergency communication, technical education, and the art of radio.
            </p>
            <div class="flex space-x-4">
                <a href="{{ '/about/' | relative_url }}" class="inline-flex items-center px-6 py-3 border border-transparent text-base font-medium rounded-md shadow-sm text-white bg-brand-800 hover:bg-brand-900">
                    Join Us
                </a>
                <a href="{{ '/contact/' | relative_url }}" class="inline-flex items-center px-6 py-3 border border-gray-300 dark:border-gray-600 shadow-sm text-base font-medium rounded-md text-gray-700 dark:text-gray-200 bg-white dark:bg-gray-700 hover:bg-gray-50 dark:hover:bg-gray-600">
                    Contact
                </a>
            </div>
        </div>
    </div>

    <!-- Next Event Card -->
    <div class="bg-brand-900 dark:bg-gray-900 shadow rounded-lg overflow-hidden p-6 text-white flex flex-col justify-between relative">
        <div>
            <h3 class="text-sm font-semibold tracking-wider text-brand-200 uppercase mb-1">Next Meeting</h3>
            <p class="text-3xl font-bold mb-2">2nd Thursday</p>
            <p class="text-lg text-brand-100">7:00 PM</p>
            <p class="text-sm text-brand-300 mt-4">
                Cole County Sheriff's Office<br>
                Training Room
            </p>
        </div>
        <div class="mt-6">
             <a href="https://www.google.com/maps/search/?api=1&query=350+E+High+St,+Jefferson+City,+MO+65101" target="_blank" class="inline-flex items-center text-sm font-medium text-white hover:text-brand-200">
                Get Directions &rarr;
            </a>
            <div class="mt-4 border-t border-brand-700 pt-4">
                 <h4 class="text-xs font-semibold tracking-wider text-brand-200 uppercase mb-1">Weekly Net</h4>
                 <p class="text-sm">Wednesdays @ 8:00 PM<br>147.000 (-) 127.3</p>
            </div>
        </div>
    </div>
</div>

<!-- Row 2: Resources, New to Radio, About -->
<div class="grid grid-cols-1 md:grid-cols-3 gap-6 mb-6">
    <!-- Resources -->
    <a href="{{ '/resources/' | relative_url }}" class="group bg-white dark:bg-gray-800 shadow rounded-lg overflow-hidden hover:shadow-lg transition-shadow duration-300">
        <div class="h-48 relative">
             <!-- Placeholder image - replace with actual resource image -->
              <div class="absolute inset-0 bg-gradient-to-br from-blue-500 to-cyan-500 flex items-center justify-center">
                  <svg class="h-16 w-16 text-white opacity-75" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 11a7 7 0 01-7 7m0 0a7 7 0 01-7-7m7 7v4m0 0H8m4 0h4m-4-8a3 3 0 01-3-3V5a3 3 0 116 0v6a3 3 0 01-3 3z" />
                  </svg>
              </div>
        </div>
        <div class="p-6">
            <h3 class="text-lg font-bold text-gray-900 dark:text-white group-hover:text-brand-800 dark:group-hover:text-brand-400">Radio Resources</h3>
            <p class="mt-2 text-sm text-gray-500 dark:text-gray-400">Frequencies, repeaters, and area nets.</p>
        </div>
    </a>

    <!-- New to Radio -->
    <a href="{{ '/new-hams/' | relative_url }}" class="group bg-white dark:bg-gray-800 shadow rounded-lg overflow-hidden hover:shadow-lg transition-shadow duration-300">
        <div class="h-48 relative">
             <div class="absolute inset-0 bg-gradient-to-br from-green-500 to-teal-500 flex items-center justify-center">
                   <svg class="h-16 w-16 text-white opacity-75" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 6.253v13m0-13C10.832 5.477 9.246 5 7.5 5S4.168 5.477 3 6.253v13C4.168 18.477 5.754 18 7.5 18s3.332.477 4.5 1.253m0-13C13.168 5.477 14.754 5 16.5 5c1.747 0 3.332.477 4.5 1.253v13C19.832 18.477 18.247 18 16.5 18c-1.746 0-3.332.477-4.5 1.253" />
                  </svg>
             </div>
        </div>
        <div class="p-6">
            <h3 class="text-lg font-bold text-gray-900 dark:text-white group-hover:text-brand-800 dark:group-hover:text-brand-400">New to Radio?</h3>
             <p class="mt-2 text-sm text-gray-500 dark:text-gray-400">Getting licensed, GMRS, and Meshtastic.</p>
        </div>
    </a>

    <!-- About -->
    <a href="{{ '/about/' | relative_url }}" class="group bg-white dark:bg-gray-800 shadow rounded-lg overflow-hidden hover:shadow-lg transition-shadow duration-300">
        <div class="h-48 relative">
             <div class="absolute inset-0 bg-gradient-to-br from-indigo-500 to-purple-500 flex items-center justify-center">
                  <svg class="h-16 w-16 text-white opacity-75" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17 20h5v-2a3 3 0 00-5.356-1.857M17 20H7m10 0v-2c0-.656-.126-1.283-.356-1.857M7 20H2v-2a3 3 0 015.356-1.857M7 20v-2c0-.656.126-1.283.356-1.857m0 0a5.002 5.002 0 019.288 0M15 7a3 3 0 11-6 0 3 3 0 016 0zm6 3a2 2 0 11-4 0 2 2 0 014 0zM7 10a2 2 0 11-4 0 2 2 0 014 0z" />
                  </svg>
             </div>
        </div>
        <div class="p-6">
            <h3 class="text-lg font-bold text-gray-900 dark:text-white group-hover:text-brand-800 dark:group-hover:text-brand-400">About the Club</h3>
             <p class="mt-2 text-sm text-gray-500 dark:text-gray-400">Our history, officers, and constitution.</p>
        </div>
    </a>
</div>

<!-- Row 3: Projects, News, Community Service -->
<div class="grid grid-cols-1 md:grid-cols-3 gap-6">
     <!-- Projects -->
    <a href="{{ '/projects/' | relative_url }}" class="group bg-white dark:bg-gray-800 shadow rounded-lg overflow-hidden hover:shadow-lg transition-shadow duration-300">
        <div class="p-6">
            <div class="flex items-center mb-4">
                 <div class="p-2 bg-orange-100 dark:bg-orange-900 rounded-lg text-orange-600 dark:text-orange-300">
                    <svg class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19.428 15.428a2 2 0 00-1.022-.547l-2.387-.477a6 6 0 00-3.86.517l-.318.158a6 6 0 01-3.86.517L6.05 15.21a2 2 0 00-1.806.547M8 4h8l-1 1v5.172a2 2 0 00.586 1.414l5 5c1.26 1.26.367 3.414-1.415 3.414H4.828c-1.782 0-2.674-2.154-1.414-3.414l5-5A2 2 0 009 10.172V5L8 4z" />
                    </svg>
                 </div>
                 <h3 class="ml-3 text-lg font-bold text-gray-900 dark:text-white">Projects</h3>
            </div>
            <p class="text-sm text-gray-500 dark:text-gray-400 mb-4">
                Check out what we're building and doing.
            </p>
            <ul class="space-y-2">
                {% for project in site.projects limit:2 %}
                <li class="text-sm text-brand-700 dark:text-brand-400 hover:underline">{{ project.title }}</li>
                {% endfor %}
            </ul>
        </div>
    </a>

    <!-- News -->
    <a href="{{ '/blog/' | relative_url }}" class="group bg-white dark:bg-gray-800 shadow rounded-lg overflow-hidden hover:shadow-lg transition-shadow duration-300">
         <div class="p-6">
            <div class="flex items-center mb-4">
                 <div class="p-2 bg-blue-100 dark:bg-blue-900 rounded-lg text-blue-600 dark:text-blue-300">
                    <svg class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 20H5a2 2 0 01-2-2V6a2 2 0 012-2h10a2 2 0 012 2v1m2 13a2 2 0 01-2-2V7m2 13a2 2 0 002-2V9a2 2 0 00-2-2h-2m-4-3H9M7 16h6M7 8h6v4H7V8z" />
                    </svg>
                 </div>
                 <h3 class="ml-3 text-lg font-bold text-gray-900 dark:text-white">News & Events</h3>
            </div>
            <p class="text-sm text-gray-500 dark:text-gray-400 mb-4">
                Latest announcements and club updates.
            </p>
             <ul class="space-y-2">
                {% for post in site.posts limit:2 %}
                <li class="text-sm text-brand-700 dark:text-brand-400 hover:underline">
                    <span class="text-gray-400 text-xs mr-1">{{ post.date | date: "%b %d" }}</span>
                    {{ post.title }}
                </li>
                {% endfor %}
            </ul>
        </div>
    </a>

    <!-- Community Service -->
    <a href="{{ '/outreach/' | relative_url }}" class="group bg-white dark:bg-gray-800 shadow rounded-lg overflow-hidden hover:shadow-lg transition-shadow duration-300">
         <div class="p-6">
             <div class="flex items-center mb-4">
                 <div class="p-2 bg-red-100 dark:bg-red-900 rounded-lg text-red-600 dark:text-red-300">
                    <svg class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4.318 6.318a4.5 4.5 0 000 6.364L12 20.364l7.682-7.682a4.5 4.5 0 00-6.364-6.364L12 7.636l-1.318-1.318a4.5 4.5 0 00-6.364 0z" />
                    </svg>
                 </div>
                 <h3 class="ml-3 text-lg font-bold text-gray-900 dark:text-white">Outreach</h3>
            </div>
            <p class="text-sm text-gray-500 dark:text-gray-400">
                Public service, emergency comms, and education.
            </p>
        </div>
    </a>
</div>
