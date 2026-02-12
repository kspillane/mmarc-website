---
layout: default
title: Club News
permalink: /blog/
---

<div class="card">
  <h1>Club News</h1>
  
<div class="bg-white dark:bg-gray-800 shadow overflow-hidden sm:rounded-lg mb-8">
  <div class="px-4 py-5 sm:px-6 border-b border-gray-200 dark:border-gray-700">
    <h1 class="text-2xl leading-6 font-medium text-gray-900 dark:text-white">Club News</h1>
  </div>
  
  <ul class="divide-y divide-gray-200 dark:divide-gray-700">
    {% for post in site.posts %}
      <li class="px-4 py-5 sm:px-6 hover:bg-gray-50 dark:hover:bg-gray-700 transition duration-150 ease-in-out">
        <div class="flex items-center justify-between">
          <div class="text-lg font-medium text-brand-800 truncate">
             <a href="{{ post.url | relative_url }}">{{ post.title | escape }}</a>
          </div>
          <div class="ml-2 flex-shrink-0 flex">
            <span class="px-2 inline-flex text-xs leading-5 font-semibold rounded-full bg-green-100 text-green-800">
              {{ post.date | date: "%b %-d, %Y" }}
            </span>
          </div>
        </div>
        <div class="mt-2 text-sm text-gray-500 dark:text-gray-400">
          {{ post.excerpt }}
        </div>
      </li>
    {% endfor %}
  </ul>
</div>
</div>
