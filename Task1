from lxml import html
import requests
data = {"username": "realgord88", "password": "Dagestan88"}
url = "http://31.23.214.207:1337/login"
h = {
	'User-Agent': 'Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/29.0.157.62 Safari/537.36)'
}
s = requests.Session()
s.headers.update(h)
r = s.post(url, data=data, headers = h)
while True:
	q=s.get("http://31.23.214.207:1337/task")
	page = html.fromstring(q.text)

	raq = page.xpath('//*[@id="taskform"]/tbody[1]/tr/th')
	for i in raq:
		wow, trash = i.text.split('=')
		answer = eval(wow)
	r = s.post('http://31.23.214.207:1337/checker', data={"answer":answer,"taskid":'1'}, headers = h)
