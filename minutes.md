---
layout: default
title: Meeting Minutes
permalink: /minutes/
---

<div class="bg-white dark:bg-gray-800 shadow overflow-hidden sm:rounded-lg">
  <div class="px-4 py-5 sm:px-6 border-b border-gray-200 dark:border-gray-700">
    <h1 class="text-2xl leading-6 font-medium text-gray-900 dark:text-white">Meeting Minutes</h1>
    <p class="mt-1 max-w-2xl text-sm text-gray-500 dark:text-gray-400">
      Archive of past meeting minutes.
    </p>
  </div>
  
  <ul class="divide-y divide-gray-200 dark:divide-gray-700">
    {% for minute in site.minutes %}
      <li class="relative px-4 py-5 sm:px-6 hover:bg-gray-50 dark:hover:bg-gray-700 transition duration-150 ease-in-out">
        <div class="flex justify-between space-x-4">
          <div class="min-w-0 flex-1">
            <a href="{{ minute.url | relative_url }}" class="block focus:outline-none">
              <span class="absolute inset-0" aria-hidden="true"></span>
              <p class="text-sm font-medium text-brand-800 truncate">{{ minute.title }}</p>
              <p class="text-sm text-gray-500 truncate">{{ minute.date | date: "%B %d, %Y" }}</p>
            </a>
          </div>
          <div>
            <!-- Heroicon: chevron-right -->
            <svg class="h-5 w-5 text-gray-400" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20" fill="currentColor" aria-hidden="true">
              <path fill-rule="evenodd" d="M7.293 14.707a1 1 0 010-1.414L10.586 10 7.293 6.707a1 1 0 011.414-1.414l4 4a1 1 0 010 1.414l-4 4a1 1 0 01-1.414 0z" clip-rule="evenodd" />
            </svg>
          </div>
        </div>
      </li>
    {% else %}
      <li class="px-4 py-5 sm:px-6 text-gray-500 text-sm italic">
        No minutes available yet.
      </li>
    {% endfor %}
  </ul>
</div>
