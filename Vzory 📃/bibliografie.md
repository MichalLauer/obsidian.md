---
Datum: {{importDate | format("YYYY-MM-DD")}}
Zdroj: [Kniha, Článek]
---
# {{ title }}{% if edition %} ({{ edition }}){% endif %}
**Autoři:** {{ authors }}
**ISBN:** {{ ISBN if ISBN else "Nedefinováno"}}
**DOI:** {{ DOI if DOI else "Nedefinováno"}}
**Zdroj:** {% if url %}[{{ url }}]({{ url }}) {% else %}Nedefinováno {% endif %}
**Zotero:** [{{ select }}]({{ select }})
{% if abstractNote -%}
## Abstrakt
{{ abstractNote }}
{% endif %}
{% if attachments -%}
## Soubory
{% for item in attachments -%}
- [{{ item.title | replace(r/\..+$/, '') }}]({{ item.pdfURI }})
{% endfor -%}
{% endif %}
# Poznámky k obsahu
...
- - -
[[{{ citekey }}|{{ bibliography | replace('**', '') | replace('_', '')}}]]