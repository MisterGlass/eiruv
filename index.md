<html>
<head>
    <title>Fair Lawn Eruv is currently {{ site.data.eruv_status.status }}</title>
    <link href="styles.css" rel="stylesheet" media="all">
</head>


<body class="status{{ site.data.eruv_status.status }}">
        <div class="eruv {{ site.data.eruv_status.status }}">
                <h2>The eruv is currently</h2>
                <h1>{{ site.data.eruv_status.status }}</h1>
                <p class="details">{{ site.data.eruv_status.details }}</p>
                <p class="date">{{ site.data.eruv_status.date }}</p>
        </div>
        <button onclick="document.getElementById('map_container').style.display = (document.getElementById('map_container').style.display == 'none' ? 'block' : 'none')">Show Eruv Map</button>
        <div id="map_container" style="display: none">
                <iframe src="https://www.google.com/maps/d/embed?mid=zEtlKkCOSY7c.kt4t89hGddOE" width="640" height="480"></iframe>
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
                                <li><a href="{{ shul.url }}" target="_blank">{{ shul.name }}</a></li>
                        {% endfor %}
                </ul>
        </div>
</body>
</html> 