<html>
<head>
<style>
/* 自定义样式 */
.no-bullet {
  list-style-type: none;
  padding-left: 0;
}

</style>
</head>
<body>

<h2 id="projects" style="margin: -15px 0 2px;">Projects</h2>

<div class="projects">
  <ul class="bibliography no-bullet">
    {% for link in site.data.projects.main %}
    <li>
      <div class="pub-row">
        <div class="col-sm-12" style="position: relative; padding: 5px;">
          {% if link.conference_short %}
          <abbr class="badge">{{ link.conference_short }}</abbr>
          {% endif %}
          {% if link.image %}
          <img src="{{ link.image }}" class="teaser img-fluid z-depth-1" style="width: {{ link.width }}px; height: auto;">
          {% endif %}
        </div>
        <div class="col-sm-12" style="position: relative; padding: 5px;">
          <div class="title">
            <a href="{{ link.pdf }}">{{ link.title }}</a>
          </div>
          <div class="author">{{ link.authors }}</div>
          <div class="periodical"><em>{{ link.conference }}</em></div>
          <div class="links">
            {% if link.code %}
            <a href="{{ link.code }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size: 15px;">CODE</a>
            {% endif %}
            {% if link.notion_blog %}
            <a href="{{ link.notion_blog }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size: 15px;">Notion Blog</a>
            {% endif %}
          </div>
        </div>

      </div>
    </li>
    {% endfor %}
  </ul>
</div>

</body>
</html>
