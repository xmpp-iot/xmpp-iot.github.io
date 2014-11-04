---
layout: home
permalink: /
mage:
  feature: wood-texture-1600x800.jpg
---

<div class="tiles">

<div class="tile">
  <h2 class="post-title">IoT based on proven technology</h2>
  <p class="post-excerpt">Takes the advantage of more than 10 years of
  profound scalability and interoperability </p>
</div><!-- /.tile -->

<div class="tile">
  <h2 class="post-title">Truly open and only one standard</h2>
  <p class="post-excerpt">XMPP is the only open community based IoT
  standard. no proprietary groups or memberships everything is on the
  [XSF foundation site ][http://XMPP.org/extensions]</p>
</div><!-- /.tile -->

<div class="tile">
  <h2 class="post-title">Every language</h2>
  <p class="post-excerpt">All software is available in any
  programming language, Servers, clients, toolkits even browser implementations</p>
</div><!-- /.tile -->

<div class="tile">
  <h2 class="post-title">Federation between domains</h2>
  <p class="post-excerpt">No other standard gives you the possibility
  to share your systems with others without creating yet another REST
  api. Only hook up certificates and your things can talk to others
  anywhere on the planet</p>
</div><!-- /.tile -->

{% for post in site.posts %}
	{% include post-grid.html %}
{% endfor %}
</div><!-- /.tiles -->
