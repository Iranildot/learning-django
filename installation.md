# 📦 Installing Django on Ubuntu

A step-by-step guide to setting up Django on an Ubuntu-based system.

---

## 🧰 1. Creating and Activating a Virtual Environment

Before installing Django, it's best practice to isolate your project using a virtual environment.

### Create the virtual environment:

```bash
python3 -m venv venv
```

### Activate the virtual environment:

```bash
source venv/bin/activate
```

> You'll know it's activated when the prompt is prefixed with `(venv)`.

---

## 📥 2. Installing Django

With the virtual environment activated, install Django using `pip`:

```bash
pip install Django
```

> You can verify the installation with:
>
> ```bash
> django-admin --version
> ```

---

## 🎉 Ready to Go!

Django is now installed and you're ready to start building your first project!

Run the following to start:

```bash
django-admin startproject myproject
```

> Replace `myproject` with your desired project name.

Happy coding! 🚀

---
