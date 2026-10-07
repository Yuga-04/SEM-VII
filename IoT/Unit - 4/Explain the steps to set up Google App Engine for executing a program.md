# Setting Up Google App Engine to Execute a Program

> **Note:** The PDF has no step-by-step setup procedure for Google App Engine. It only says that App Engine is Google's **PaaS** platform for building and deploying applications in languages such as **Python, Java and Go**, that web apps run in **Google data centres**, and that Google APIs use **OAuth 2.0** with credentials from the Developers Console. The steps below are **(general knowledge)** and are kept short.

## 1. What the PDF Says
- **Google App Engine** is a **PaaS** that lets developers run websites in Google data centres without managing servers.
- It has built-in scalability and developer tools, and is a public cloud example.
- Google services are accessed through **client libraries** and need **credentials** from the Developers Console.

## 2. Setup Steps (general knowledge)

**Step 1: Create a Google account and a Cloud project**
- Sign in to the Google Cloud Console and create a new project (for example `my-first-app`).

**Step 2: Enable billing and the App Engine API**
- Link a billing account (a free tier is available).
- Enable the **App Engine Admin API** and create the App Engine application.
- Choose a **region**, which cannot be changed later.

**Step 3: Install the Google Cloud SDK**
- Install the `gcloud` command-line tool and run:
```
gcloud init
gcloud config set project my-first-app
```

**Step 4: Write the program**
- Choose a language runtime (Python, Java, Go, etc.). A minimal Python example:
```python
# main.py
from flask import Flask
app = Flask(__name__)

@app.route("/")
def hello():
    return "Hello, App Engine!"
```
- Add `requirements.txt` containing `Flask`.

**Step 5: Create the configuration file**
- `app.yaml` tells App Engine which runtime to use:
```yaml
runtime: python312
```

**Step 6: Test locally (optional)**
```
python main.py
```

**Step 7: Deploy**
```
gcloud app deploy
```
- Confirm the prompts. The code is uploaded and App Engine provisions the servers.

**Step 8: Run and view the program**
```
gcloud app browse
```
- The app runs at `https://my-first-app.appspot.com` (the URL is based on the project ID).

**Step 9: Monitor and manage**
- Use the Console to view logs, versions and traffic, and to stop or delete the app.

## 3. Flow Summary

```
Create project → Enable App Engine → Install SDK → Write code
      → app.yaml → Test locally → gcloud app deploy → Run on cloud
```

## 4. Benefits (from the PDF)
- No hardware or infrastructure management.
- Automatic scaling on demand.
- Pay-per-use pricing.
- Supports several languages such as Python, Java and Go.

## 5. Conclusion
Google App Engine is a PaaS where you create a project, enable App Engine, write the program with an `app.yaml` configuration, and deploy it with `gcloud app deploy`. Google then handles servers, scaling and maintenance, so you only focus on the code.
