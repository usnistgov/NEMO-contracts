# NEMO Contracts

[![Code style: black](https://img.shields.io/badge/code%20style-black-000000.svg)](https://github.com/psf/black)
[![PyPI - Python Version](https://img.shields.io/pypi/pyversions/NEMO-contracts?label=python)](https://www.python.org/downloads/release/python-3110/)
[![PyPI](https://img.shields.io/pypi/v/nemo-contracts?label=pypi%20version)](https://pypi.org/project/NEMO-contracts/)
[![Changelog](https://img.shields.io/github/v/tag/usnistgov/NEMO-contracts?include_prereleases&label=changelog)](https://github.com/usnistgov/NEMO-contracts/tags)

Plugin for NEMO allowing facility managers to keep track of service contracts, procurement and contractors

## Installation

```bash
python -m install nemo-contracts
```

in `settings.py` add to `INSTALLED_APPS`:

```python
INSTALLED_APPS = [
    '...',
    'NEMO_contracts',
    # 'NEMO.apps.contracts' Remove old dependency
    '...'
]
```

To enabled reminder emails, set a cron job daily with one of the following options:

1. send an authenticated http request to `<nemo_url>/email_contract_reminders/`
2. run command `django-admin send_email_contract_reminders` or `python manage.py send_email_contract_reminders`

Example of `systemd` service and timer files are provided for your convenience in the [systemd folder](https://github.com/usnistgov/NEMO-contracts/tree/master/resources/systemd).

## Usage

Add a new landing page choice or use the `Administration -> Contracts & procurements` link

# Tests

To run the tests:
```bash
python runtests.py
```
