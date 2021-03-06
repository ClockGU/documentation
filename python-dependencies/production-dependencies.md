---
description: Aufzählung und Erläuterung der benutzten Python Pakete
---

# Production Dependencies

In der Production Version werden 15 python-Pakete genutzt, welche im Folgenden aufgelistet und kurz erläutert werden.

| Paketname | Homepage | Erläuterung |
| :--- | :--- | :--- |
| django | [djangoproject](https://www.djangoproject.com/) | Basis-Webframework des Projektes |
| gunicorn | [gunicorn](https://gunicorn.org/) | WSGI HTTPS Server |
| gevent | [gevent](http://www.gevent.org/) |  |
| raven | [raven](https://docs.sentry.io/clients/python/) | Client zur Benutzung von Sentry |
| whitenoise | [whitenoise](http://whitenoise.evans.io/en/stable/) | Bereitstellung von statischen Dateien |
| django-restframework | [DRF](https://www.django-rest-framework.org) | Basis Framework für die REST-API |
| django-guardian | [django-guardian](https://django-guardian.readthedocs.io/en/stable/overview.html) | Erweiterte Rechteverwaltung |
| django-rest-framework-simplejwt | [simplejwt](https://github.com/davesque/django-rest-framework-simplejwt) | JSON Web Token Implementation für DRF |
| django-environ | [django-environ](https://django-environ.readthedocs.io/en/latest/) | Verbesserte Nutzung von Umgebungsvariablen |
| djoser | [djoser](https://djoser.readthedocs.io/en/stable/getting_started.html) | Out-of-the-Box User Login/Logout/Passwort Handling |
| python-dateutil | [dateutil](https://github.com/dateutil/dateutil) | Erweiterte Funktionen für die Verarbeitung von Zeit/Datum |
| django-anymail | [anymail](https://github.com/anymail/django-anymail) | Schnittstelle zu bekannten Email Service Providern \(ESP\) |
| django-taggit | [taggit](https://github.com/alex/django-taggit) | Einfache Verwaltung von userdefinierten Tags |
| psycopg2 | [psycopg2](http://initd.org/psycopg/docs/) | Datenbankadapter für PostgreSQL |
| psycopg2-binary | [psycopg2-binary](http://initd.org/psycopg/docs/) | Binary Split von Psycopg2 |

