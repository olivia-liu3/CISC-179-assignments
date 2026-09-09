# first code


```python
print("All the world's a stage,")
print("And all the men and women merely players:")
print("They have their exits and their entrances;")
print("And one man in his time plays many parts,")
print("His acts being seven ages.")
```

# single print() statement

```python
print("All the world's a stage,","And all the men and women merely players:","They have their exits and their entrances;
","And one man in his time plays many parts,","His acts being seven ages.", sep="\n")
```

# predict the output
127.0.0.1

# Using flush=True and flush=False
When creating counters or want user to see activity, use 
```python
flush=True
```

When only want user to see the complete final result, use
```python
flush=False
```

# understanding flush
Setting end="" reveals the buffer effect because it prevents a newline forming for each object when printing. By default end is set to "\n" which makes flush=False and flush=True look like they have the same effect. 

# challenges
- understanding what flush exactly is (figured it out by rewatching video segment)
- realizing by default sep=" ", but when after setting sep to something, there is no more space unless you write in a space
