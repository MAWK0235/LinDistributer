# LinDistributor: Accelerate and Organize LinPeas Enumeration

Tired of the game of jumping between systems during a pentest with LinPeas? Look no further! Introducing LinDistributor – your go-to solution to expedite the LinPeas enumeration process while maintaining impeccable organization. Say goodbye to delays and the tedious hunt for results one by one. With LinDistributor, do it all at once and reclaim valuable time to focus on other tasks!

## Key Features

- **Fast Enumeration**: LinDistributor speeds up the LinPeas enumeration process, ensuring quicker results without compromising accuracy.

- **Organized Results**: Keep your findings neatly organized, eliminating the need to sift through individual outputs. LinDistributor streamlines the enumeration results for easy analysis.

- **Versatile Targeting**:
  - Singular Targets: Enumerate individual targets effortlessly.
  - Target Lists: Handle multiple targets seamlessly.
  - Target Subnets: Streamline enumeration across entire subnets efficiently.

- **RSA Authentication Support**: LinDistributor supports RSA authentication, providing flexibility and security in your enumeration efforts.

## Installation

```bash
gitclone 
pip install -r requirements.txt
```

## Usage


## Command Line Arguments

- `-lp` or `--local_LinPath`: Path to the LinPeas file you would like to distribute (required).
- `-up` or `--upload_Path`: The directory to write LinPeas results to (required).
- `-t` or `--target`: Specify the target host, supporting singular targets, target lists, and target subnets.
- `-tl` or `--target_List`: The target list to run LinPeas on.
- `-u` or `--username`: Provide the username for authentication (required).
- `-p` or `--password`: Supply the password for authentication.
- `-R` or `--RSA`: The RSA key to authenticate with.
- `-P` or `--port`: Specify the SSH port for the LinPeas enumeration process (default: 22).

### Examples

Explore some examples to get started quickly.

```bash
# Enumerate a single target with LinPeas
python LinDistributer.py -lp /path/to/linpeas.sh -up /output/directory -t 192.168.1.1 -u user -p pass -P 2222

# Enumerate multiple targets from a list using RSA authentication
python LinDistributer.py -lp /path/to/linpeas.sh -up /output/directory -tl targets.txt -u user -R /path/to/private_key -P 2222

# Enumerate an entire subnet with LinPeas
python LinDistributer.py -lp /path/to/linpeas.sh -up /output/directory -t 192.168.1.0/24 -u user -p pass -P 2222


## Examples

Explore some examples to get started quickly.

```bash
# Enumerate a single target
python LinDistributer.py --target 192.168.1.1 --username user --password pass --port 22

# Enumerate multiple targets from a list
python LinDistributer.py --targetList targets.txt --username user --password pass --port 22

# Enumerate an entire subnet
python LinDistributer.py --target 192.168.1.0/24 --username user --password pass --port 22
```

