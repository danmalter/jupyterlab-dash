# jupyterlab_dash

A JupyterLab extension for rendering Plotly Dash apps as a separate window in JupyterLab :tada:

![JupyterLab and Dash Demo Video](https://user-images.githubusercontent.com/1280389/47668836-da9f4280-db7f-11e8-8523-8663b6a5347f.gif)

**Note:**: This extension does not currently support Windows or Python 2

## Prerequisites

* JupyterLab


## Installation

We haven't published the component yet, but we will soon. In the meantime, you'll need to clone the repo and install manually:

```bash
git clone https://github.com/plotly/jupyterlab-dash
cd jupyterlab-dash
npm install
npm run build
jupyter labextension link .
```

To rebuild the package and the JupyterLab app:

```bash
npm run build
jupyter lab build
```

## Usage

```python
import jupyterlab_dash
viewer = jupyterlab_dash.AppViewer(port=8050)

app = dash.Dash(__name__)

app.layout = html.Div('Hello World')

viewer.show(app)
```
