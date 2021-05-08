# QuickStart Django

* ## Windows | Unix or MacOS:
    + ### start commands on **Windows** with **`py`**.
    + ### start commands on **Unix *or* MacOS** with **`python`**.

1. ## Creating Virtual Environments:
    font: [Python Venv](https://docs.python.org/3/tutorial/venv.html)
    ***
    *
        ### Windows:
        +
            ```bash
            py -m venv .venv
            ```
            ### ***Activate .venv:***
            ***

            ### cmd:
            -
                ```cmd
                .venv\Scripts\activate.bat
                ```
            ###  git-bash:
            -
                ```bash
                source .venv/Scripts/activate.bat
                ```
    *
        ### Unix or MacOS:
        +
            ```bash
            python3 -m venv .venv
            ```
            ### ***Activate .venv:***
            ***
            -
                ```bash
                source .venv/bin/activate
                ```
        ***
    *
        ### ***Disable .venv:***
        +
            ```bash
            deactivate
            ```

2. ## (Optional) Upgrade pip in .venv:
    font: [Installing Pip](https://pip.pypa.io/en/stable/installing/#upgrading-pip)
    ***
    *
        ```bash
        py -m pip install -U pip
        ```


3. ## Install Django
    font: [Installing Django](https://docs.djangoproject.com/en/3.2/topics/install/#installing-official-release)
    ***
    *
        ### ***Once you have created a virtual environment, you need to activate it, (.venv).***
        +
            ```bash
            py -m pip install Django
            ```


## Font: [Django Tutorial](https://docs.djangoproject.com/en/3.2/intro/tutorial01/#writing-your-first-django-app-part-1a)
* ### ___Common Commands___

1. ## Start Django Project and APP:
    #### (./QuickStart-Django/)
    ***
    1.
        ```bash
        django-admin startproject mysite
        ```
    2.
        ```bash
        py manage.py startapp polls
        ```

2. ## The Development Server:
    #### (./QuickStart-Django/mysite)
    ***
    *
        ```bash
        py manage.py runserver
        ```

3. ## Change Your Models (in models.py).
    ***
    *
        Run:
        ```bash
        py manage.py makemigrations
        ```
        > To create migrations for those changes.
    *
        Run:
        ```bash
        py manage.py migrate
        ```
        > To apply those changes to the database.

4. ## Creating an Admin User.
    Quick Link: [Creanting an Admin User](https://docs.djangoproject.com/en/3.2/intro/tutorial02/#creating-an-admin-user)
    ***
    *
        ```bash
        py manage.py createsuperuser
        ```
    ### Start the development server.
    > Now, open a Web browser and go to “**/admin/**” on your local domain – e.g., *http://127.0.0.1:8000/admin/*.

## **Vs Code Config**
* ### Installed Extensions:
    1. Python
    1. Django
    1. Beautify

* ### Settings:
    #### (./QuickStart-Django/.vscode)
    * settings.json:
    ```json
    "python.pythonPath": ".\\.venv\\Scripts\\python.exe",
    "files.associations": {
        "**/templates/*.html": "django-html",
        "**/templates/*": "django-txt"
    },
    "emmet.includeLanguages": {
        "django-html": "html"
    },
    "beautify.language": {
        "js": {
            "type": [
                "javascript",
                "json"
            ],
            "filename": [
                ".jshintrc",
                ".jsbeautifyrc"
            ]
        },
        "css": [
            "css",
            "scss"
        ],
        "html": [
            "htm",
            "html",
            "django-html"
        ]
    },
    ```
