# Django polls

A historical Django tutorial application for creating questions, voting on
choices, and viewing results. The `mysite` project mounts the polls application
at `/polls/` and Django's administration interface at `/admin/`.

## Repository layout

- `polls/models.py`: questions and choices, including vote counts.
- `polls/views.py`, `polls/urls.py`, and `polls/templates/`: voting pages.
- `polls/tests.py`: application tests.
- `mysite/settings.py`: project settings and local SQLite configuration.
- `manage.py`: Django management entry point.

## Running and maintenance

This repository does not include a dependency manifest. The source uses legacy
Django APIs, including `django.conf.urls.patterns` and a `ForeignKey` without
an explicit `on_delete` argument. It needs a compatible historical environment
or a port before it can run on current Django; installing the latest Django
alone is not a verified setup procedure.

Once a compatible isolated development environment has been established, the
usual management commands are:

```sh
python manage.py migrate
python manage.py createsuperuser
python manage.py runserver 127.0.0.1:8000
python manage.py test polls
```

The database and admin account are created locally. These commands and legacy
dependency compatibility were not exercised during the documentation update.
Review configuration and dependencies before deploying this tutorial project.
