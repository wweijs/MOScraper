# Define a top-level target that depends on all outputs
all: Action_data.xlsx choco.xlsx

# Target to create Action_data.xlsx from Action.ipynb
Action_data.xlsx: Action.ipynb
	jupyter nbconvert --to notebook --execute Action.ipynb --output Action_data.ipynb
	# Ensure Action.ipynb generates Action_data.csv during its execution

# Target to create choco.csv from Scraper Choco Totaal.ipynb
choco.xlsx: Scraper\ Choco\ Totaal.ipynb
	jupyter nbconvert --to notebook --execute "Scraper Choco Totaal.ipynb" --output choco.ipynb
	# Ensure Scraper Choco Totaal.ipynb generates choco.csv during its execution

# Clean up choco.csv, and Action_data.csv if needed
clean:
	rm -f choco.xlsx Action_data.xlsx
