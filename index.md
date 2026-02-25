
---
layout: default
---

<div class="homepage">
	<header class="page-header">
		<h1>Avi Fishman</h1>
		<p class="tagline">Essays worth reading</p>
		<a href="mailto:avi.fishman63@gmail.com" class="email-link">avi.fishman63@gmail.com</a>
	</header>

	{% if site.posts.size > 0 %}
	<div class="posts-container">
		{% for post in site.posts limit:10 %}
		<article class="post-item">
			<a href="{{ post.url | relative_url }}">
				<h2>{{ post.title }}</h2>
				<time>{{ post.date | date: "%B %-d, %Y" }}</time>
			</a>
		</article>
		{% endfor %}
	</div>
	{% endif %}
</div>

