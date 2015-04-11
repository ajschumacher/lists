# set diagram / vertical venn

(maybe seaborn?)

http://setosa.io/blog/2014/08/03/csv-fingerprints/
https://github.com/setosa/csv-fingerprint


import pandas as pd

def settable(*sets):
  """Returns a set table as a DataFrame"""
  sets = [set(x) for x in sets]
  elements = sorted(list(reduce(lambda x, y: x | y, sets)))
  table = [[element in x for x in sets] for element in elements]
  df = pd.DataFrame(table, index=elements)
  return df


from __future__ import unicode_literals

x = x.sort(columns=range(x.shape[1]), ascending=False)

x = settable(roman, greek, russian)

plt.axis('off')
i = imshow(x, interpolation="nearest", extent=[0,100,0,100], cmap="YlGn")

http://en.wikipedia.org/wiki/Greek_alphabet
ΑΒΓΔΕΖΗΘΙΚΛΜΝΞΟΠΡΣΤΥΦΧΨΩ
http://en.wikipedia.org/wiki/ISO_basic_Latin_alphabet
ABCDEFGHIJKLMNOPQRSTUVWXYZ
http://en.wikipedia.org/wiki/Russian_alphabet
АБВГДЕЁЖЗИЙКЛМНОПРСТУФХЦЧШЩЪЫЬЭЮЯ

common denominator version
ABCDEFGHIJKLMNOPQRSTUVWXYZ
ABΓΔEZHΘIKΛMNΞOΠPΣTYΦXΨΩ
AБBΓДEЁЖЗИЙKЛMHOΠPCTYΦXЦЧШЩЪЫЬЭЮЯ

Russian "У" as "Y" is questionable...
