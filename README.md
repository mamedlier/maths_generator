#! C:/Python/python

import cgi
import random

form = cgi.FieldStorage()

print('Content-type: text/html\n\n')
print('''<!DOCTYPE html>
<html lang="ru">
<head>
<meta charset="utf-8">
<title>Генератор примеров</title>
<style>
span {font-weight: bold; font-size: 24px;}
</style>
</head>
<body>
<p>&nbsp;</p>
<form method="POST" action="maths_generator.py">
<p><input type="submit" value="Генерация примера"></p>
</form>
<p>Пример: <span>''', random.randint(1, 100), random.choice(['+', '-', '/', '**', '%', '//']), random.randint(1, 100), '''</span></p>
</body>
</html>''')
