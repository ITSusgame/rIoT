---
layout: page
title: Archive
---

<html lang="it">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Archive - Il mio sito</title>
    <script>
        // Definisci la stringa di benvenuto
        var benvenuto = 
"            WHAT EXACTLY ARE YOU LOOKING FOR HERE ????\n" +
"\n" +
"            ___           _,.---,---.,_\n" +
"            |         ,;~'             '~;, \n" +
"            |       ,;                     ;,\n" +
"   Frontal  |      ;                         ; ,--- Supraorbital Foramen\n" +
"    Bone    |     ,'                         /'\n" +
"            |    ,;                        /' ;,\n" +
"            |    ; ;      .           . <-'  ; |\n" +
"            |__  | ;   ______       ______   ;<----- Coronal Suture\n" +
"           ___   |  '/~\"     ~\" . \"~     \"~\\'  |\n" +
"           |     |  ~  ,-~~~^~, | ,~^~~~-,  ~  |\n" +
" Maxilla,  |      |   |        }:{        | <------ Orbit\n" +
"Nasal and  |      |   l       / | \\       !   |\n" +
"Zygomatic  |      .~  (__,.--\" .^. \"--.,__)  ~.\n" +
"  Bones    |      |    ----;' / | \\ `;-<--------- Infraorbital Foramen\n" +
"           |__     \\__.       \\/^\\/       .__/\n" +
"              ___   V| \\                 / |V <--- Mastoid Process\n" +
"              |      | |T~\\___!___!___/~T| |\n" +
"              |      | |`IIII_I_I_I_IIII'| |\n" +
"     Mandible |      |  \\,III I I I III,/  |\n" +
"              |       \\   `~~~~~~~~~~'    /\n" +
"              |         \\   .       . <-x---- Mental Foramen\n" +
"              |__         \\.    ^    ./\n" +
"                            ^~~~^~~~^";
;

        // Stampa la stringa di benvenuto nella console quando si apre gli strumenti di sviluppo
        console.log(benvenuto);
    </script>
</head>
<body>

<section>
  {% if site.posts[0] %}

    {% capture currentyear %}{{ 'now' | date: "%Y" }}{% endcapture %}
    {% capture firstpostyear %}{{ site.posts[0].date | date: '%Y' }}{% endcapture %}
    {% if currentyear == firstpostyear %}
        <h3>Posts di quest'anno</h3>
    {% else %}  
        <h3>{{ firstpostyear }}</h3>
    {% endif %}

    {%for post in site.posts %}
      {% unless post.next %}
        <ul>
      {% else %}
        {% capture year %}{{ post.date | date: '%Y' }}{% endcapture %}
        {% capture nyear %}{{ post.next.date | date: '%Y' }}{% endcapture %}
        {% if year != nyear %}
          </ul>
          <h3>{{ post.date | date: '%Y' }}</h3>
          <ul>
        {% endif %}
      {% endunless %}
        <li><time>{{ post.date | date:"%d %b" }} - </time>
          <a href="{{ post.url | prepend: site.baseurl | replace: '//', '/' }}">
            {{ post.title }}
          </a>
        </li>
    {% endfor %}
    </ul>

  {% endif %}
</section>

</body>
</html>
