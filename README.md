# Maskpw

A simple library to ask the user for a password. Similar to getpass.getpass() but allows to specify a default mask (like \* instead of blank).

## Features 🧰

-   Customize prompt showed to the user.
-   Use a custom mask to hide the password.

## Installation 📦⬇

Use [pip](https://pip.pypa.io/en/stable/) to install it.

```bash
python3 -m pip install maskpw
```

## Usage 🛠

To use it, just import the `get_password` function and call it with a prompt (`"Password: "` by default):

```python
from maskpw import get_password

if __name__ == "__main__":
    username = input("Username: ")
    password = get_password()
    print(f"Username: {username}; Password: {password}")
```

This will show the following:

```console
$ python test.py
Username: John Doe
Password: *****
Username: John Doe; Password: 12347
```

If you want to change the mask:

```python
from maskpw import get_password

if __name__ == "__main__":
    username = input("Username: ")
    password = get_password(mask="#")
    print(f"Username: {username}; Password: {password}")
```

Now it will look like:

```console
$ python test.py
Username: John Doe
Password: #####
Username: John Doe; Password: 12347
```

## Contributing ✍

[Pull requests](https://github.com/harmony5/maskpw/pulls/new) are welcome. For major changes, [bug fixes](https://github.com/harmony5/maskpw/issues/new?template=bug_report.md&labels=bug&projects=harmony5%2Fmaskpw%2F1) or [feature requests](https://github.com/harmony5/maskpw/issues/new?template=feature_request.md&projects=harmony5%2Fmaskpw%2F1), please open an issue first to discuss what you would like to change.

## License 📜⚖

This project uses the [MIT](https://choosealicense.com/licenses/mit) license.
