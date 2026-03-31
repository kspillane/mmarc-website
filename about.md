---
layout: default
title: About Us
permalink: /about/
officers:
  - name: "Tim Raymer"
    callsign: "KAØOUV"
    role: "President"
  - name: "Bryan Braunschweig"
    callsign: "WØESE"
    role: "Vice President"
  - name: "Rich Glassner"
    callsign: "NØEAX"
    role: "Sec/Treasurer"
  - name: "Jim Biggerstaff"
    callsign: "NØTKN"
    role: "Trustee"
board_members:
  - name: "Art Langston"
    callsign: "KDØGY"
    role: "Past President (Term Ends Dec 2023)"
  - name: "Steve Hick"
    callsign: "WWØG"
    role: "Term Ends Dec 2024"
  - name: "Jim Biggerstaff"
    callsign: "NØTKN"
    role: "Term Ends Dec 2026"
  - name: "Jim Branson"
    callsign: "N0LBY"
    role: "Term Ends Dec 2028"
tech_committee:
  - name: "Jim Biggerstaff"
    callsign: "NØTKN"
    role: "Chairman"
  - name: "Tim Raymer"
    callsign: "KAØOUV"
    role: "Member"
  - name: "Jack Boswell"
    callsign: "NØKSF"
    role: "Member"
managers:
  - name: "Stephen Hick"
    callsign: "WWØG"
    role: "2 Meter Net Manager"
  - name: "Mike Smith"
    callsign: "ADØYM"
    role: "VE Liaison"
  - name: "Kent Trimble"
    callsign: "K9ZTV"
    role: "Special Events Coordinator"
  - name: "John S. Graves"
    callsign: "kbØnxk"
    role: "Web Master"
---

<div class="bg-white dark:bg-gray-800 shadow overflow-hidden sm:rounded-lg mb-8">
  <div class="px-4 py-5 sm:px-6">
    <h3 class="text-lg leading-6 font-medium text-gray-900 dark:text-white">About MMARC</h3>
    <p class="mt-1 max-w-2xl text-sm text-gray-500 dark:text-gray-400">
      The Mid-MO Amateur Radio Club is a non-profit organization dedicated to the promotion of Amateur Radio used for emergency communication, experimentation, and social interaction.
    </p>

    <h3 class="text-lg leading-6 font-medium text-gray-900 dark:text-white mt-6">Mission Statement</h3>
    <p class="mt-1 max-w-2xl text-sm text-gray-500 dark:text-gray-400">
      Advancing amateur radio through community engagement, technical education, and emergency preparedness. We empower individuals to master the airwaves and serve our community through the power of wireless technology.
    </p>

    <!-- Club Callsigns Section -->
    <div class="mt-6 pt-4 border-t border-gray-200 dark:border-gray-700">
      <h4 class="text-md leading-5 font-medium text-gray-900 dark:text-white mb-3">Club Callsigns</h4>
      <div class="grid grid-cols-1 md:grid-cols-2 gap-4">
        <div class="bg-gray-50 dark:bg-gray-700/50 p-4 rounded-md">
          <div class="text-sm font-semibold text-brand-800 dark:text-brand-400">MidMoARC Special Event Callsign</div>
          <div class="text-lg font-bold text-gray-900 dark:text-white my-1">NØSS</div>
          <div class="text-xs text-gray-500 dark:text-gray-400 italic">In Memory of Tom Hammond</div>
        </div>
        <div class="bg-gray-50 dark:bg-gray-700/50 p-4 rounded-md">
          <div class="text-sm font-semibold text-brand-800 dark:text-brand-400">MidMoARC Repeater Callsign</div>
          <div class="text-lg font-bold text-gray-900 dark:text-white my-1">KØETY</div>
          <div class="text-xs text-gray-500 dark:text-gray-400 italic">In Memory of Don Dulle SK</div>
        </div>
      </div>
    </div>
  </div>
</div>

<div class="grid grid-cols-1 md:grid-cols-2 gap-6 pb-12">
  
  <!-- Officers -->
  <div class="bg-white dark:bg-gray-800 shadow overflow-hidden sm:rounded-lg">
    <div class="px-4 py-5 sm:px-6 border-b border-gray-200 dark:border-gray-700">
      <h3 class="text-lg leading-6 font-medium text-gray-900 dark:text-white">Club Officers</h3>
    </div>
    <ul class="divide-y divide-gray-200 dark:divide-gray-700">
      {% for item in page.officers %}
      <li class="px-4 py-4 sm:px-6">
        <div class="text-sm text-gray-900 dark:text-white font-medium">{{ item.name }}{% if item.callsign %} ({{ item.callsign }}){% endif %}</div>
        <div class="text-xs text-gray-500 dark:text-gray-400">{{ item.role }}</div>
      </li>
      {% endfor %}
    </ul>
  </div>

  <!-- Board Members -->
  <div class="bg-white dark:bg-gray-800 shadow overflow-hidden sm:rounded-lg">
    <div class="px-4 py-5 sm:px-6 border-b border-gray-200 dark:border-gray-700">
      <h3 class="text-lg leading-6 font-medium text-gray-900 dark:text-white">Board Members</h3>
    </div>
    <ul class="divide-y divide-gray-200 dark:divide-gray-700">
      {% for item in page.board_members %}
      <li class="px-4 py-4 sm:px-6">
        <div class="text-sm text-gray-900 dark:text-white font-medium">{{ item.name }}{% if item.callsign %} ({{ item.callsign }}){% endif %}</div>
        <div class="text-xs text-gray-500 dark:text-gray-400">{{ item.role }}</div>
      </li>
      {% endfor %}
    </ul>
  </div>

  <!-- Tech Committee -->
  <div class="bg-white dark:bg-gray-800 shadow overflow-hidden sm:rounded-lg">
    <div class="px-4 py-5 sm:px-6 border-b border-gray-200 dark:border-gray-700">
      <h3 class="text-lg leading-6 font-medium text-gray-900 dark:text-white">Tech Committee</h3>
    </div>
    <ul class="divide-y divide-gray-200 dark:divide-gray-700">
      {% for item in page.tech_committee %}
      <li class="px-4 py-4 sm:px-6">
        <div class="text-sm text-gray-900 dark:text-white font-medium">{{ item.name }}{% if item.callsign %} ({{ item.callsign }}){% endif %}</div>
        <div class="text-xs text-gray-500 dark:text-gray-400">{{ item.role }}</div>
      </li>
      {% endfor %}
    </ul>
  </div>

  <!-- Managers & Coordinators -->
  <div class="bg-white dark:bg-gray-800 shadow overflow-hidden sm:rounded-lg">
    <div class="px-4 py-5 sm:px-6 border-b border-gray-200 dark:border-gray-700">
      <h3 class="text-lg leading-6 font-medium text-gray-900 dark:text-white">Managers & Coordinators</h3>
    </div>
    <ul class="divide-y divide-gray-200 dark:divide-gray-700">
      {% for item in page.managers %}
      <li class="px-4 py-4 sm:px-6">
        <div class="text-sm text-gray-900 dark:text-white font-medium">{{ item.name }}{% if item.callsign %} ({{ item.callsign }}){% endif %}</div>
        <div class="text-xs text-gray-500 dark:text-gray-400">{{ item.role }}</div>
      </li>
      {% endfor %}
    </ul>
  </div>

</div>
