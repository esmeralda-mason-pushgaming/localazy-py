# localazy-py
Python test for the localazy api

## Dependencies
Requires `python3`

## Running
To use run from the root with
```
python3 main.py
```
Setup localazy CLI tools using
```
npm @localazy/cli
```

To download the translation information from the "Jiggly's Pot O' Gold" project run
```
npx localazy download
```

The [config](localazy.json) specifies the download folder of all the files.

Each "download file" is a JSON for a specific language with all the keys.