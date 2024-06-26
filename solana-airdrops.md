---
git-date: 2019-05-20T22:02:39-07:00
layout: default
title: "Solana Airdrops: Most Comprehensive 101 Guide"
metadescription: 101 Guide to Solana Airdrops - Most Comprehensive list covering significant airdrops. Our approach is no bullshit airdrops on Solana. We don't waste our own time and don't want to waste yours. We list only high-quality Solana ecosystem projects where tokens make sense and meaningful airdrops are highly likely.
permalink: solana-airdrops
h1title: Solana Airdrops
pagetitle: "Solana Airdrops: Most Comprehensive 101 Guide"
featured-image: /images/blog/solana-airdrops.png
---

<h1>{{ page.h1title }}</h1>

<section class="section-tickers">
  <p>Our approach is no bullshit airdrops on Solana. We don't waste our own time and don't want to waste yours. We list only high-quality Solana ecosystem projects where tokens make sense and meaningful airdrops are highly likely.</p>
  <div class="container-tickers">
    <table class="table-tickers">
      <thead>
        <tr>
          <th>Project</th>
          <th>Category</th>
          <th>Venture Funding</th>
          <th>URL</th>
          <th>Twitter</th>
          <th>What to do?</th>
        </tr>
      </thead>
      <tbody>

      {% assign solana_airdrops = site.airdrops | where_exp:"item", "item.ecosystem contains 'solana'" %}
      {% for solana_airdrops in solana_airdrops %}
        <tr class="ticker-row">
          <td > {{ solana_airdrops.title }} </td>
          <td > {{ solana_airdrops.category }}  </td>
          <td > {{solana_airdrops.raised}} from {{solana_airdrops.investors }} </td>
          <td > <a href="{% if solana_airdrops.reflink %} {{solana_airdrops.reflink}} {% else %}
{{solana_airdrops.project_url}} {% endif %}">{{solana_airdrops.project_url | remove: 'https://'}}</a> </td>
          <td > <a href="https://twitter.com/{{ solana_airdrops.twitter_handle }}">@{{ solana_airdrops.twitter_handle }}</a> </td>
          <td > {{ solana_airdrops.todo | markdownify }} Read more: <a href="/airdrop/{{ solana_airdrops.title | remove:  ' ' | capitalize }}">{{ solana_airdrops.h1title}}</a></td>
        </tr>
      {% endfor %}
      </tbody>
    </table>

  </div>
</section>
