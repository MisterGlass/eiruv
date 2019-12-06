<html>
<head>
    <title>Fair Lawn Eruv is currently {{ site.data.eruv_status.status }}</title>
</head>


<body style = "
        {% if site.data.eruv_status.status == 'Up' %}
                background-color: green;
        {% elsif site.data.eruv_status.status == 'Down' %}
                background-color: red;
        {% endif %}
">
        <div class="eruv {{ site.data.eruv_status.status }}">
                <h2>The eruv is currently</h2>
                <h1>{{ site.data.eruv_status.status }}</h1>
                <p class="details">{{ site.data.eruv_status.details }}</p>
                <p class="date">{{ site.data.eruv_status.date }}</p>
        </div>
        <button>Show Eruv Map</button>
        <div id="map_container" style="display: none">
                ADD MAP EMBED HERE
        </div>
        <div class="info">
                <span>The Fair Lawn Eruv is inspected every Friday.</span>
                <span>For more information you can call our hotline at <a>201-254-9190</a></span>
                <span>Sign up for our weekly newsletter <a href="mailto:fairlawneruv+subscribe@groups.io">by sending an email with your name in the subject line</a></span>
        </div>
        <div class="shuls">
                The Fair Lawn Eruv is maintained as a community service by the following synagogues. For more information on a particular synagogue or to arrange a visit to the community, please click on the synagogue’s name below.
                <ul>
                        {% for shul in site.data.shuls %}
                                <li><a href="{{ shul.link }}" target="_blank">{{ shul.name }}</a></li>
                        {% endfor %}
                </ul>
        </div>
</body>
</html> 