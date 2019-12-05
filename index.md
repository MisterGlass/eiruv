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
</body>

</html> 