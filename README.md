Scons-Protoc
============

Scons tool for compiling Google's Protobuf

Put the ```protoc.py``` file in ```#site_scons/site_tools/``` then in your SConstruct file do something like:

```python

env = Environment(
  tools = ['default', 'protoc'],
  #...
  )
  
protoc_cc = env.Protoc(["src/Example.proto"],                                
    PROTOC_PATH='#src',                                                      
    PROTOC_CCOUT='#src',                                                     
    )  

```