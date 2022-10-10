## How To Get Attribute in Beautifulsoup


```python
# ********** 👇 Beautifulsoup Get Attribute 👇 ********** #


from bs4 import BeautifulSoup # 👉️ Import BeautifulSoup module




# -- 👇 Beautifulsoup Get attributes of a tag  👇 -- #


# 👇 HTML Source
html = '''

<div id="node">
<p>Hello Beautifulsoup</p>
</div>

'''

soup = BeautifulSoup(html, 'html.parser') # 👉️ Parsing

el = soup.find("div") # 👉️ Find <div>

div_attrs = el.attrs # 👉️ Get div Attributes

print(div_attrs) # 👉️ Print Result

# 👆 Output: {'id': 'node'}



# 👇 HTML Source
html = '''

<div id="node" class="col">
<p>Hello Beautifulsoup</p>
</div>

'''

soup = BeautifulSoup(html, 'html.parser') # 👉️ Parsing

el = soup.find("div") # 👉️ Find <div>

div_attrs = el.attrs # 👉️ Get div Attributes

print(div_attrs) # 👉️ Print Result

# 👆 Output: {'id': 'node', 'class': ['col']}


print("Class:", div_attrs["class"]) # 👉️ Print Class Attribute

# 👆 Output: Class: ['col']


print("ID:", div_attrs["id"]) # 👉️ Print ID Attribute

# 👆 Output: ID: node







# -- 👇 Beautifulsoup Get By Attribute Value  👇 -- #


# 👇 HTML Source
html = '''

<div id="node">
<p>Hello Beautifulsoup</p>
</div>

'''

soup = BeautifulSoup(html, 'html.parser') # 👉️ Parsing

el = soup.find(attrs={"id" : "node"}) # 👉️ Get By Attribute Value

print(el) # 👉️ Print

# 👇 Output
'''
<div id="node">
<p>Hello Beautifulsoup</p>
</div>
'''




# 👇 HTML Source
html = '''

<div id="node" class="root">
<p>Hello Beautifulsoup</p>
</div>
'''

soup = BeautifulSoup(html, 'html.parser') # 👉️ Parsing

el = soup.find(attrs={"id": "node", "class": ["root"]}) # 👉️ Get By Multiple Attribute Value

print(el) # 👉️ Print

# 👇 Output
'''
<div class="root" id="node">
<p>Hello Beautifulsoup</p>
</div>
'''






# -- 👇 Beautifulsoup Get By existing attribute  👇 -- #


# 👇 HTML Source
html = '''

<div id="node">
<p>Hello Beautifulsoup</p>
</div>
'''

soup = BeautifulSoup(html, 'html.parser') # 👉️ Parsing

el = soup.find(attrs={"id": True}) # 👉️ Get IF Attribute ID exist

print(el) # 👉️ Print

# 👇 Output
'''
<div id="node">
<p>Hello Beautifulsoup</p>
</div>
'''




# 👇 HTML Source
html = '''

<div id="node" class="root">
<p>Hello Beautifulsoup</p>
</div>
'''

el = soup.find(attrs={"id": True, "class": True}) # 👉️ Get IF Attribute ID and Class exist

print(el) # 👉️ Print

# 👆 Output: None
```

For the tutorial of the examples, vists [Beautifulsoup Get Attribute - PyTutorial](https://pytutorial.com/beautifulsoup-get-attribute)
