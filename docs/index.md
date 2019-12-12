---
---

<html>
<head>
    <title>Fair Lawn Eruv is currently {{ site.data.eruv_status.status }}</title>
    <link href="styles.css" rel="stylesheet" media="all">
</head>


<body class="status{{ site.data.eruv_status.status | upcase }}">
        <div class="main">
                <div class="eruv {{ site.data.eruv_status.status }}">
                        <h2>Fair Lawn Eruv</h2>
                        <h3>The Eruv Is:</h3>
                        <h1>{{ site.data.eruv_status.status }}</h1>
                        <p class="details">{{ site.data.eruv_status.details }}</p>
                        <p class="date">The last inspection was completed on: <strong>{{ site.data.eruv_status.date }}</strong></p>
                </div>
                <button onclick="document.getElementById('map_container').style.display = (document.getElementById('map_container').style.display == 'none' ? 'block' : 'none')">Show Eruv Map</button>
                <div id="map_container" style="display: none">
                        <iframe src="https://www.google.com/maps/d/embed?mid=zEtlKkCOSY7c.kt4t89hGddOE" width="640" height="480"></iframe>
                </div>
        </div>
        <footer>
                <div class="shuls">
                        The Fair Lawn Eruv is maintained as a community service by the following synagogues. For more information on a particular synagogue or to arrange a visit to the community, please click on the synagogue’s name below.
                        <ul>
                                {% for shul in site.data.shuls %}
                                        <li><a href="{{ shul.url }}" target="_blank">{{ shul.name }}</a></li>
                                {% endfor %}
                        </ul>
                </div>
                <div class="info">
                        <p>The Fair Lawn Eruv is inspected every Friday.</p>
                        <p>Fair Lawn Eruv Hotline: <a href="tel:201-254-9190">201-254-9190</a></p>
                        <p>Other eruv questions? <a href="mailto:info@fairlawneruv.org">Email the Eruv Inspector</a> or call <a href="tel:201-757-8365">201-757-8365</a></p>
                </div>
                <div class="subscribe">
                        <p><a href="mailto:fairlawneruv+subscribe@groups.io?subject=Please Put Your Name Here">Sign up for our weekly newsletter</a></p>
                        <p class="copyright">&copy; {{ 'now' | date: "%Y" }} Fair Lawn Eruv. All Rights Reserved.</p>
                </div>
        </footer>
</body>
</html> 