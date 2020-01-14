{% assign months = 'January|February|March|April|May|June|July|August|September|October|November|December' | split: '|' %}


## 100 Club Winners {{ year[0] }}

{% for year in site.data.100club %}

### {{ year[0] }}

  {% for row in year[1] %}
    {%- unless row.month and row.number and row.name -%}
      {%- continue -%}
    {%- endunless -%}
    {%- assign month_num = row.month | minus: 1 -%}
    {%- assign month = months[month_num] -%}
{{ month }} | {{ row.number }} | {{ row.name }}
  {% endfor %}

{% endfor %}

