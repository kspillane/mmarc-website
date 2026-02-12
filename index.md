---
layout: default
title: Home
---

<!-- Hero Section -->
<div class="bg-white dark:bg-gray-800 overflow-hidden shadow rounded-lg mb-8">
  <div class="px-4 py-5 sm:p-6 text-center">
    <h1 class="text-3xl font-extrabold text-gray-900 dark:text-white sm:text-4xl">
      Welcome to the Mid-MO Amateur Radio Club
    </h1>
    <p class="mt-4 max-w-2xl mx-auto text-xl text-gray-500 dark:text-gray-300">
      We are the Mid-MO Amateur Radio Club (K0ETY), located in Jefferson City, MO. We are a group of amateur radio enthusiasts dedicated to the hobby and serving our community.
    </p>
    <div class="mt-8 flex justify-center">
      <div class="inline-flex rounded-md shadow">
        <a href="{{ '/about/' | relative_url }}" class="inline-flex items-center justify-center px-5 py-3 border border-transparent text-base font-medium rounded-md text-white bg-brand-800 hover:bg-brand-900">
          Learn More
        </a>
      </div>
      <div class="ml-3 inline-flex">
        <a href="{{ '/contact/' | relative_url }}" class="inline-flex items-center justify-center px-5 py-3 border border-transparent text-base font-medium rounded-md text-brand-800 bg-brand-100 hover:bg-brand-200">
          Contact Us
        </a>
      </div>
    </div>
  </div>
</div>

<div class="grid grid-cols-1 gap-6 sm:grid-cols-2 lg:grid-cols-3">
  <!-- Repeater Info -->
  <div class="bg-white dark:bg-gray-800 overflow-hidden shadow rounded-lg">
    <div class="px-4 py-5 sm:p-6">
      <h3 class="text-lg leading-6 font-medium text-gray-900 dark:text-white">Repeater Info</h3>
      <div class="mt-2 max-w-xl text-sm text-gray-500 dark:text-gray-300">
        <p><strong>VHF:</strong> 147.000 MHz (-), 127.3 Hz Tone</p>
        <p class="mt-2"><strong>UHF:</strong> 442.150 MHz (+), 127.3 Hz Tone</p>
      </div>
    </div>
  </div>

  <!-- Meeting Info -->
  <div class="bg-white dark:bg-gray-800 overflow-hidden shadow rounded-lg">
    <div class="px-4 py-5 sm:p-6">
      <h3 class="text-lg leading-6 font-medium text-gray-900 dark:text-white">Join Us</h3>
      <div class="mt-2 max-w-xl text-sm text-gray-500 dark:text-gray-300">
        <p>Meetings are held every month at 7 p.m. on the Second Thursday in the Training Room of the Cole County Sheriff's Office.</p>
      </div>
    </div>
  </div>

  <!-- Events -->
  <div class="bg-white dark:bg-gray-800 overflow-hidden shadow rounded-lg">
    <div class="px-4 py-5 sm:p-6">
      <h3 class="text-lg leading-6 font-medium text-gray-900 dark:text-white">Upcoming Events</h3>
      <div class="mt-2 max-w-xl text-sm text-gray-500 dark:text-gray-300">
        <p><strong>Weekly Net:</strong> Every Wednesday at 8:00 PM on the 147.000 repeater.</p>
      </div>
    </div>
  </div>
</div>

<!-- Latest News -->
<div class="mt-8 bg-white dark:bg-gray-800 overflow-hidden shadow rounded-lg">
  <div class="px-4 py-5 sm:px-6 border-b border-gray-200 dark:border-gray-700">
    <h3 class="text-lg leading-6 font-medium text-gray-900 dark:text-white">Latest News</h3>
  </div>
  <ul class="divide-y divide-gray-200 dark:divide-gray-700">
    {% for post in site.posts limit:3 %}
      <li class="px-4 py-4 sm:px-6 hover:bg-gray-50 dark:hover:bg-gray-700 transition duration-150 ease-in-out">
        <div class="flex items-center justify-between">
          <div class="text-sm font-medium text-brand-800 truncate">
            <a href="{{ post.url | relative_url }}">{{ post.title | escape }}</a>
          </div>
          <div class="ml-2 flex-shrink-0 flex">
            <span class="px-2 inline-flex text-xs leading-5 font-semibold rounded-full bg-green-100 text-green-800">
              {{ post.date | date: "%b %-d, %Y" }}
            </span>
          </div>
        </div>
        <div class="mt-2 sm:flex sm:justify-between">
          <div class="sm:flex">
            <p class="flex items-center text-sm text-gray-500 dark:text-gray-400">
              {{ post.excerpt | strip_html | truncatewords: 20 }}
            </p>
          </div>
        </div>
      </li>
    {% endfor %}
  </ul>
  <div class="bg-gray-50 dark:bg-gray-900 px-4 py-4 sm:px-6">
    <div class="text-sm">
      <a href="{{ '/blog/' | relative_url }}" class="font-medium text-brand-800 hover:text-brand-900">View all news <span aria-hidden="true">&rarr;</span></a>
    </div>
  </div>
</div>
