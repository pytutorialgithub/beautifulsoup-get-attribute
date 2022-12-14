## How To Get Attribute in Beautifulsoup


```python
# ********** π Beautifulsoup Get Attribute π ********** #


from bs4 import BeautifulSoup # ποΈ Import BeautifulSoup module




# -- π Beautifulsoup Get attributes of a tag  π -- #


# π HTML Source
html = '''

<div id="node">
<p>Hello Beautifulsoup</p>
</div>

'''

soup = BeautifulSoup(html, 'html.parser') # ποΈ Parsing

el = soup.find("div") # ποΈ Find <div>

div_attrs = el.attrs # ποΈ Get div Attributes

print(div_attrs) # ποΈ Print Result

# π Output: {'id': 'node'}



# π HTML Source
html = '''

<div id="node" class="col">
<p>Hello Beautifulsoup</p>
</div>

'''

soup = BeautifulSoup(html, 'html.parser') # ποΈ Parsing

el = soup.find("div") # ποΈ Find <div>

div_attrs = el.attrs # ποΈ Get div Attributes

print(div_attrs) # ποΈ Print Result

# π Output: {'id': 'node', 'class': ['col']}


print("Class:", div_attrs["class"]) # ποΈ Print Class Attribute

# π Output: Class: ['col']


print("ID:", div_attrs["id"]) # ποΈ Print ID Attribute

# π Output: ID: node







# -- π Beautifulsoup Get By Attribute Value  π -- #


# π HTML Source
html = '''

<div id="node">
<p>Hello Beautifulsoup</p>
</div>

'''

soup = BeautifulSoup(html, 'html.parser') # ποΈ Parsing

el = soup.find(attrs={"id" : "node"}) # ποΈ Get By Attribute Value

print(el) # ποΈ Print

# π Output
'''
<div id="node">
<p>Hello Beautifulsoup</p>
</div>
'''




# π HTML Source
html = '''

<div id="node" class="root">
<p>Hello Beautifulsoup</p>
</div>
'''

soup = BeautifulSoup(html, 'html.parser') # ποΈ Parsing

el = soup.find(attrs={"id": "node", "class": ["root"]}) # ποΈ Get By Multiple Attribute Value

print(el) # ποΈ Print

# π Output
'''
<div class="root" id="node">
<p>Hello Beautifulsoup</p>
</div>
'''






# -- π Beautifulsoup Get ByΒ existingΒ attribute  π -- #


# π HTML Source
html = '''

<div id="node">
<p>Hello Beautifulsoup</p>
</div>
'''

soup = BeautifulSoup(html, 'html.parser') # ποΈ Parsing

el = soup.find(attrs={"id": True}) # ποΈ Get IF Attribute ID exist

print(el) # ποΈ Print

# π Output
'''
<div id="node">
<p>Hello Beautifulsoup</p>
</div>
'''




# π HTML Source
html = '''

<div id="node" class="root">
<p>Hello Beautifulsoup</p>
</div>
'''

el = soup.find(attrs={"id": True, "class": True}) # ποΈ Get IF Attribute ID and Class exist

print(el) # ποΈ Print

# π Output: None
```

For the tutorial of the examples, vists [Beautifulsoup Get Attribute - PyTutorial](https://pytutorial.com/beautifulsoup-get-attribute)
