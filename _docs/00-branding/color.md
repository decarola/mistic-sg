---
title: Colori
info: Colori ufficiale e le varianti disponibili.
colors: 
  - name: Colori base
    items:
    - name: $bianco
      hex: 'efefef'
    - name: $ottanio
      hex: '508894'
    - name: $grigio
      hex: '230209' 
  - name: Varianti di ottone
    items:
    - name: $ottanio-light-1
      hex: '508894'  
    - name: $ottanio-light-2
      hex: '7aacb7'  
    - name: $ottanio-light-3
      hex: 'abcbd2'  
    - name: $ottanio-light-4
      hex: 'ddeaed'  
  - name: Varianti di grigio
    items:
    - name: $grigio-light-1
      hex: '23050B'  
    - name: $grigio-light-2
      hex: '604B50'  
    - name: $grigio-light-3
      hex: '978B8E'  
    - name: $grigio-light-4
      hex: 'D8D5D6'  
---

<section class="sg-branding">
  {% for group in page.colors %} 
  <div>
    <h3>{{ group.name | capitalize }}</h3>
    <ul class="color-set">
    {% for item in group.items %}
      <li>
        <div style="background:#{{ item.hex }}"></div> 
        <p><code>{{ item.name }}</code></p>
        {% if item.hex %}<p>#{{ item.hex }}</p>{% endif %}
        {% if item.pretty %}<p>{{ item.pretty }}</p>{% endif %}
        {% if item.rgb %}<p>{{ item.rgb }}</p>{% endif %}
      </li>
    {% endfor %}
    </ul>
  </div>
  {% endfor %}
</section>