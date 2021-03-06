# Summary

A barebones Flask app that demonstrates some basic Folium functionality using the WMATA API. This exact repository is hosted on Heroku [here](http://whorl.herokuapp.com).

The core of this demo is the Jupyter notebook (`demo.ipynb`). It goes into depth, with links, comments, and examples including GeoJSON/choropleths and the Walk Score API. An HTML version of the notebook is available as `demo.html`.

The rest of the repo takes one of those examples and shows how it can be delivered through a web browser. The code is meant to showcase possibilities, not best practices. Don't judge me.

## Environment

The project was developed under Python 2.7 on Ubuntu 16.04.

An environment is provided in `environment.yml`. Using Conda you can run `conda env create -f environment.yml` to create a virtual environment with all the dependencies for both the Flask app and Jupyter notebook.

## References

The higher level technologies used are:
* [Conda](https://conda.io/docs/) for package management
* [Git](https://git-scm.com/) for version control
* [Heroku](https://www.heroku.com) for web hosting
* [Jupyter](http://jupyter.org) for interactive Python notebooks

See the Jupyter notebook for links to documentation relevant to the demos, including Flask, Folium, and links to the APIs used.

### Heroku quickstart

To push a repository to Heroku, the following files are important:
* `Procfile`
* `runtime.txt`
* `requirements.txt`
* `conda-requirements.txt`

(*Suggested*) Use the [Conda buildpack](https://github.com/kennethreitz/conda-buildpack). If you choose not to, put all requirements into `requirements.txt`.

Note that the Conda buildpack is being deprecated in favor of a Docker implementation.

Download the [Heroku CLI](https://devcenter.heroku.com/articles/heroku-cli) and sign in with `heroku login`.

Create a Heroku application with `heroku create <app_name>` or leave blank to auto-generate a name.

Deploy the repo to Heroku by `git push heroku master`. You should be able to access your app at `https://<app_name>.herokuapp.com`.

There is a [quickstart guide](https://devcenter.heroku.com/articles/getting-started-with-python-o) available as a reference.

## Debugging

You can run Flask apps locally by eg. `python app.py`. This app will run at `localhost:33507`.

`heroku logs` can display remote logs from your app, however `heroku local` will run the app at `localhost:5000` and will be more useful for debugging.
