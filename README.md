# jAndroid

jAndroid is a taint analysis tool for template matching against android apps.

The current use case is to identify potential logic bug exploit chains on Android.

## Installation

jAndroid requires Python 3.4 or later to run.

1. Clone the repository
2. Install the required python packages by running the following command:
```bash
pip install -r requirements.txt
```
3. Place any apps you want to analyze in the `apps` directory or connect an Android device with USB debugging enabled


# Usage
Please check out the Project Wiki for detailed instructions on how to use the tool.


## neo4j Output (Recommended)
To run the tool with neo4j and the defaut templates, you need to have neo4j installed and running on your machine.   
You can install neo4j by following the instructions [here](https://neo4j.com/docs/operations-manual/current/installation/).   
Or using docker by running the following command:  
`docker run  --restart always  --publish=7474:7474 --publish=7687:7687  --env NEO4J_AUTH=neo4j/n3o4jn3o4j neo4j`

```bash
python3 src/jandroid.py -g neo4j
```
The output can then be found at `localhost:7474` in your browser using the default credentials `neo4j/n3o4jn3o4j`

## HTML Output
To run the tool with the default templates, simply run the following command:

```bash
python3 src/jandroid.py
```

The output can then be found at `output/graph/jandroid.html`