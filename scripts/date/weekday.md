{% set day = now().weekday() %}
{% set date = now().date().strftime("%d-%m-%Y") %}
Oggi è
{% if (day == 0) %}
lunedì, {{ date }}
{% elif (day == 1) %}
martedì, {{ date }}
{% elif (day == 2) %}
mercoledì, {{ date }}
{% elif (day == 3) %}
giovedì, {{ date }}
{% elif (day == 4) %}
venerdì, {{ date }}
{% elif (day == 5) %}
sabato, {{ date }}
{% elif (day == 6) %}
domenica, {{ date }}
{% endif %}
