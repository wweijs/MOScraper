SHELL := /bin/bash

# Define a top-level target that depends on all outputs
all: Action_data.xlsx choco.xlsx Berrie.xlsx

# Target to create Action_data.xlsx from Action.ipynb
Action_data.xlsx: Action.ipynb
	jupyter nbconvert --to notebook --execute Action.ipynb --output - 
	# Ensure Action.ipynb generates Action_data.xlsx during its execution

# Target to create choco.xlsx from Scraper Choco Totaal.ipynb
choco.xlsx: Scraper\ Choco\ Totaal.ipynb
	jupyter nbconvert --to notebook --execute "Scraper Choco Totaal.ipynb" --output - 
	# Ensure Scraper Choco Totaal.ipynb generates choco.xlsx during its execution

# Target to create Berrie.xlsx from BerrieScrape.ipynb"
Berrie.xlsx: BerrieScrape.ipynb
	jupyter nbconvert --to notebook --execute BerrieScrape.ipynb --output - 
	# Ensure Scraper Choco Totaal.ipynb generates Berrie.xlsx during its execution


# Clean up choco.xlsx, and Action_data.xlsx if needed
clean:
	rm -f choco.xlsx Action_data.xlsx Berrie.xlsx


