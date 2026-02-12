---
layout: default
title: Home
---

<div class="card">
  <h1>Welcome to the Mid-MO Amateur Radio Club</h1>
  <p>We are the Mid-MO Amateur Radio Club (K0ETY), located in Jefferson City, MO. We are a group of amateur radio enthusiasts dedicated to the hobby and serving our community.</p>
  <div class="grid-2">
    <div>
        <h2>Join Us</h2>
        <p>Meetings are held every month at 7 p.m. on the Second Thursday in the Training Room of the Cole County Sheriff's Office.</p>
        <a href="{{ '/about/' | relative_url }}" class="btn">Learn More</a>
    </div>
    <div>
        <h2>Repeater Info</h2>
        <p><strong>VHF:</strong> 147.000 MHz (-), 127.3 Hz Tone</p>
        <p><strong>UHF:</strong> 442.150 MHz (+), 127.3 Hz Tone</p>
    </div>
  </div>
</div>

<div class="card">
  <h2>Upcoming Events</h2>
  <p>Check back soon for upcoming club events and nets.</p>
  <p><strong>Weekly Net:</strong> Every Wednesday at 8:00 PM on the 147.000 repeater.</p>
</div>

<div class="card">
  <h2>Latest News</h2>
  <ul>
    {% for post in site.posts limit:3 %}
      <li>
        <span class="post-meta">{{ post.date | date: "%b %-d, %Y" }}</span>
        <h3>
          <a class="post-link" href="{{ post.url | relative_url }}">
            {{ post.title | escape }}
          </a>
        </h3>
        {{ post.excerpt }}
      </li>
    {% endfor %}
  </ul>
  <p><a href="{{ '/blog/' | relative_url }}">View all news</a></p>
</div>
