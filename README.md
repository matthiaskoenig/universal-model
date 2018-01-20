# universal-model
Working with the BiGG universal model
Based on discussion here
https://groups.google.com/forum/#!topic/cobra-pie/8oanj0H5q4A



You can access it via the BiGG API (http://bigg.ucsd.edu/data_access).
Find an example in the attached notebook.

- is there some interface to browse the information, i.e., some BiGG
> site to browse the information (or are the listed reactions in BiGG
> basically the universal model?)
The universal model is basically the entirety of the BiGG database and
all reactions are set to be irreversible.
> - how do I build a model using these reactions? I.e., how do I start
> from scratch with an empty model and add reactions?
> - do I have to handle the species separately?
You can add species separately but it is probably more error prone. When
you add a reaction its metabolites are added for you (cf. notebook).
> - what are the available algorithms to add reactions programatically,
> i.e. things like gap-fill, ... 

# Setup
Create virtualenv
```
cd universal-model
mkvirtualenv universal-model --python=python3
workon universal-model
```

Setup ipython kernel and jupyterlab
```
pip install -r requirements.txt --upgrade
pip install ipykernel>=4.8.0
pip install jupyterlab>=0.31.1
python -m ipykernel install --user --name=universal-model
jupyter serverextension enable --py jupyterlab --sys-prefix
```

Run jupyterlab
```
jupyter lab
```
