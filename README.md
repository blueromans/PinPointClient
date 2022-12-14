[![PyPI version](https://img.shields.io/pypi/v/PinPointClient.svg)](https://pypi.python.org/pypi/PinPointClient)

# PinPointClient Python PyPackage

PinPoint is Aws Sms Service. PinPointClient is a Python library to access services quickly.

## Installation

Use the package manager [pip](https://pip.pypa.io/en/stable/) to install foobar.

```bash
pip install PinPointClient
```
## Environment Variables

```bash
REGION: aws region
PINPOINT_MESSAGE_TYPE: message type
PINPOINT_APPLICATION_ID: application id
AWS_ACCESS: aws access key id
AWS_SECRET: aws secret access key
CHANNEL_TYPE: channel type
```
### Note
If you don't want to set this variables from global environment you can pass them to class.
You can see usage below
## Usage

```python
from pinpoint import GsmService
kwargs = {
    # you can also set region from environment.
    'region': 'region', # Default value : 'eu-central-1'
    # you can also set message type from environment.
    'message_type': 'message type',  # Default value : 'TRANSACTIONAL'
    # you can also set channel type from environment.
    'channel_type': 'channel type',  # Default value : 'SMS' 
    # you can also set application id type from environment.
    'applicationId': 'application id',  # Default value : None
     # you can also set aws access key id type from environment.
    'aws_access': 'aws access key id',  # Default value : None
    # you can also set aws secret access key type from environment.
    'aws_secret': 'aws secret access key',  # Default value : None
}
gsm_service = GsmService(**kwargs)
gsm_service.send(phone='Phone Number (+905551234567)', message='Your Message')
```

## Contributing

Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

## License

[MIT](https://choosealicense.com/licenses/mit/)
