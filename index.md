
---
layout: default
---

<section class="homepage">
	<div class="hero-minimal">
		<h1>Avi Fishman</h1>
		<p class="subtitle">Thoughtful essays on ideas worth exploring</p>
		
		<div class="about-card">
			<p>I write about technology, ideas, and things I find interesting. Here you'll find essays that attempt to be clear, honest, and worth your time.</p>
			<div class="contact-info">
				<a href="mailto:avi.fishman63@gmail.com" class="email-link">avi.fishman63@gmail.com</a>
			</div>
		</div>
	</div>

	{% if site.posts.size > 0 %}
	<section class="essays-section">
		<h2>Latest Essays</h2>
		<div class="essays-list">
			{% for post in site.posts limit:8 %}
			<article class="essay-item">
				<a href="{{ post.url | relative_url }}" class="essay-link">
					<h3>{{ post.title }}</h3>
					<p class="essay-date">{{ post.date | date: "%B %-d, %Y" }}</p>
					<p class="essay-excerpt">{{ post.excerpt | strip_html | truncate: 160 }}</p>
				</a>
			</article>
			{% endfor %}
		</div>
		{% if site.posts.size > 8 %}
		<div class="view-all">
			<a href="/posts/" class="link-secondary">View all essays →</a>
		</div>
		{% endif %}
	</section>
	{% endif %}
</section>

