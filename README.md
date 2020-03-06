# Module9_surfs_up
Python Jupyter Notebook, VS Code, Github, SQLite

from matplotlib import style

style.use('fivethirtyeight')


import matplotlib.pyplot as plt
import numpy as np
import pandas as pd

import datetime as dt

import sqlalchemy
from sqlalchemy.ext.automap import automap_base
from sqlalchemy.orm import session
from sqlalchemy import create_engine, func

engine = create_engine("sqlite:///hawaii.sqlite")

Base = automap_base()

Base.prepare(engine, reflect=True)

Base.classes.keys()


Measurement = Base.classes.measurement
Station = Base.classes.station

session = Session(engine)

