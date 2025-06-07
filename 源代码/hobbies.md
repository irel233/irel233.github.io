---
layout: default
title: 我的爱好
---

<section class="hobbies-section">
    <h2>兴趣爱好</h2>
    <div class="hobbies-grid">
        {% for hobby in site.hobbies %}
        <figure class="hobby-card">
            <img src="{{ hobby.image | relative_url }}" alt="{{ hobby.title }}" class="hobby-image">
            <figcaption>
                <h3>{{ hobby.title }}</h3>
                <p>{{ hobby.description }}</p>
            </figcaption>
        </figure>
        {% endfor %}
    </div>
    
    <aside class="hobby-stats">
        <h3>爱好统计</h3>
        <ul>
            {% for stat in site.data.stats %}
            <li>{{ stat.name }}：<meter value="{{ stat.value }}" min="{{ stat.min }}" max="{{ stat.max }}">{{ stat.value }}{{ stat.unit }}</meter></li>
            {% endfor %}
        </ul>
    </aside>
</section> 