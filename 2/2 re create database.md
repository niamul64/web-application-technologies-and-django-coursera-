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