
### model creating:<br>
<img width="500" src= "pic/model or data base in django.JPG"/>
<br><br>

### model detail checking:

<br>
<img width="500" src= "pic/model detail check.JPG"/>
<br><br>

### value inserting :
<br> most important command python manage.py shell<br>
now from shell we can insert value to data base<br>

<br>
<img width="500" src= "pic/inserting a row in table.JPG"/>
<br><br>

### এখন, কি কি element/value ইনপুট দিতে পারব তা check করা যাবে:

<br>
<img width="500" src= "pic/check which type of values i could give input.JPG"/>
<br><br>

### more command and function of models:

<br>
<img width="500" src= "pic/more function of models.JPG"/>
<br><br>

### Models data type:

<br>
<img width="500" src= "pic/data type.JPG"/>


<br><br><br><br>
all commands togater : https://www.dj4e.com/lectures/DJ-02-Model-Single.txt
<br><br><br>

#### reset the data base: $ rm db.sqlite3  
<br><br>
now, make data base table in models.py: (example)
<br>
<br>
from django.db import models<br>

class Question(models.Model):<br>
    question_text = models.CharField(max_length=200)<br>
    pub_date = models.DateTimeField('date published')<br>


class Choice(models.Model):<br>
    question = models.ForeignKey(Question, on_delete=models.CASCADE)<br>
    choice_text = models.CharField(max_length=200)<br>
    votes = models.IntegerField(default=0)<br>

<br>
<br>
And we have to  register these tables at admin.py<br>
from django.contrib import admin<br>

from .models import Question<br>
admin.site.register(Question)<br><br>

NOW, by creating super user we can insert data and do other task.
<br>
<br>
<br>

# OR,
<br>

### we also can use shell to do: 
<br>
$ python manage.py shell 
<br>
see more at: 
<a href="https://docs.djangoproject.com/en/3.0/intro/tutorial02/">https://docs.djangoproject.com/en/3.0/intro/tutorial02/</a>


<br><br><br><br>

## if the models /database gets messed up(যদি table গুলা বানাতে যেয়ে কোন ভুল করে ফেলি তাহলে ):
<br>
প্রথমে django প্রোজেক্ট ফাইল  এ থেকে , <br>
python manage.py check
<br>যদি no issues হয়য় তাহলে <br>

## rm */migrations/00* <br>
## rm db.sqlite3 <br>
## ls -l */models.py <br>
#Now edit the models and : create the data base again
## python manage.py makemigrations<br>
##python manage.py migrat<br>

