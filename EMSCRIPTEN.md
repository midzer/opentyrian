# Emscripten

## Build

```
emmake make
```

## Link

```
emcc -flto -O3 -fno-rtti -fno-exceptions *.o -o index.html -sUSE_SDL=2 -sASYNCIFY -sASYNCIFY_IGNORE_INDIRECT -sENVIRONMENT=web --preload-file data/ -sEXPORTED_RUNTIME_METHODS=['allocate'] -sASYNCIFY_ONLY=@../funcs.txt -sSTACK_SIZE=131072 --closure 1
```
