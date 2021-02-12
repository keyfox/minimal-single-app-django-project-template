# Minimal Single-App Django Project Template

## Getting started

### Put project name into placeholder

In this template, a word `shyguy` is used as a placeholder for the name of your project.

The following script substitutes every `shyguy` with either `my_awesome_app` or `MyAwesomeApp`.

```bash
snakecase='my_awesome_app'
camelcase='MyAwesomeApp'

grep -rl shyguy . | \
  xargs sed -i \
            -e "s/shyguy/${snakecase}/g" \
            -e "s/Shyguy/${camelcase}/g"
```

### Setup envfile

In this template, `settings.py` loads `.env` file using `python-decouple`

If you just want to run Django application anyway, use `.env.sample`.
(Of course it's not suitable for production.)

```
cp .env.sample .env
```

### Let's do this

```
pip3 install -r requirements.txt
./manage.py runserver
```
