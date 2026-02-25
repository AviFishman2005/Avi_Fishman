
---
layout: home
---

<section class="hero">
	<div class="inner">
		<h1>Avi Fishman</h1>
		<p class="tagline">Essays that I think are worth writing.</p>
		<a class="cta" href="/about/">About</a>
	</div>
</section>

<section class="posts-list">
	<h2>Recent Essays</h2>
	<ul class="cards">
		{% for post in site.posts limit:6 %}
			<li class="card">
				<a href="{{ post.url | relative_url }}">
					<h3>{{ post.title }}</h3>
					<p class="excerpt">{{ post.excerpt | strip_html | truncate: 140 }}</p>
					<p class="meta">{{ post.date | date: "%B %-d, %Y" }}</p>
				</a>
			</li>
		{% endfor %}
	</ul>
</section>

