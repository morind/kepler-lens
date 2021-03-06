# kepler-lens
A python utility to load and update Kepler/K2 data to Warp10

```bash
python main.py --help          
Usage: main.py [OPTIONS] COMMAND [ARGS]...

Options:
  --help  Show this message and exit.

Commands:
  init
  update

python main.py init --help                        
Usage: main.py init [OPTIONS] DATASET

Options:
  --token TEXT     warp WRITE token
  --endpoint TEXT  warp endpoint
  --path TEXT      kepler download folder
  --limit TEXT     comma separated list of compagne to download.
  --help           Show this message and exit.
```

# Example

```
python main.py init k2 --path /home/debian/.kepler \ 
                       --endpoint https://example.org --wtoken WRITEABCD
                       
python main.py init kepler --path /home/debian/.kepler \
                           --endpoint https://example.org --wtoken WRITEABCD --limit C1

python main.py update --rtoken READACBD \
                           --endpoint https://example.org --wtoken WRITEABCD --limit 400
```
