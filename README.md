pgBoardUnchained
================

After years of mucking with the PHP flavor of pgBoard, I decided to rewrite it in Python for Django 1.6, and leverage node, redis and socket.io to make the board experience much neater. The text only approach is still in play with twitter bootstrap leading the styling charge. 

**To setup pgBoardUnchained:**

1. Install and set up postgres (9.3 or higher): `brew install postgres`

2. Install node: `brew install node`

3. Install npm: `pip install npm`

4. Install redis-server: `brew install redis`

5. Configure database with vivalavinyl.settings.__init__.py values: `include ~/vivalavinyl/vivalavinyl/settings/__init__.py`

6. Install Python.

7. Install virtualenv:

```
brew install virtualenv
pip install virtualenvwrapper
export WORKON_HOME=~/Envs
mkdir -p $WORKON_HOME
source /path/to/virtualenvwrapper.sh
```

8. Clone project:

```
cd ~
mkdir code
cd code
mkdir pgBoardUnchained
git clone https://github.com/DarthHater/pgBoardUnchained.git
```

9. Run `mkvirtualenv pgboard`.

10. Run `workon pgboard`.

11. In `pgboard`, install modules:

```
npm install cookie
npm install socket.io
pip install redis
pip install -r /path/to/project/requirements.txt
```

12. Run `python /path/to/project/manage.py migrate board`.

12. In a new terminal window, `cd` to nodejs and node thread.js.

13. In another terminal window, run `sudo redis-server /usr/local/etc/redis.conf`.
