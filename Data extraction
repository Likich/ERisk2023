import os
import xml.etree.ElementTree as ElementTree
import pandas as pd

def flatten(l):
    return [item for sublist in l for item in sublist]

def collect_data(location): 
  all_posts = []
  ids = []
  for filename in os.listdir(location):
    all_texts = []
    all_ids = []
    with open(location + '/' + filename, 'r') as f:   # Reading file
      xml = f.read()
      xml = '<ROOT>' + xml + '</ROOT>'   # Let's add a root tag
      root = ElementTree.fromstring(xml)
      # Simple loop through each document
      for doc in root:
        all_texts.append(doc.find('TEXT').text.strip())
        all_ids.append(doc.find('DOCNO').text.strip())
    all_posts.append(all_texts)
    ids.append(all_ids)
  posts = flatten(all_posts)
  ids = flatten(ids)
  df = pd.DataFrame({'sentence-id': ids, 'text': posts})
  return df


