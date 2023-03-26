# UrlShortener
#Url Shortener using Python and Cuttly API key
import requests


def shorten_link(full_link, link_name):
    API_KEY = "ffb9990a27af247fccae19a36145d75076856"
    BASE_URL = "https://cutt.ly/api/api.php"

    payload = {'key': API_KEY, 'short': full_link, 'name': link_name}
    request = requests.get(BASE_URL, params=payload)
    data = request.json()

    print(data)


shorten_link('https://en.wikipedia.org/wiki/Python_(programming_language)', 'jkl')
