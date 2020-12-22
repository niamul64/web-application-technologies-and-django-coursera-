
code:<br>
def hello(request) :<br>
<br>
 <tb>   num_visits = request.session.get('num_visits', 0) + 1<br>
    request.session['num_visits'] = num_visits<br>
    if num_visits > 4 : del(request.session['num_visits'])<br>
<br><br>
    resp = HttpResponse('view count='+str(num_visits))<br>
    resp.set_cookie('dj4e_cookie', 'eb530d95', max_age=1000)<br>
<br>
    return resp<br>