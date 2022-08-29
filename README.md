# `aws-cfn-bootstrap` with updated requests module for ubuntu 22.04
source page: https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/releasehistory-aws-cfn-bootstrap.html#releasehistory-aws-cfn-bootstrap-v1

source init archive: https://s3.amazonaws.com/cloudformation-examples/aws-cfn-bootstrap-py3-2.0-15.tar.gz

requests module version: `2.28.1`

aws-cfn-bootstrap-py3 version: `2.0-15`


## This updated fix the next issue:

```
Traceback (most recent call last):
  File "/usr/local/bin/cfn-signal", line 20, in <module>
    from cfnbootstrap.cfn_client import CloudFormationClient
  File "/usr/local/lib/python3.10/dist-packages/cfnbootstrap/cfn_client.py", line 24, in <module>
    from cfnbootstrap import aws_client, util
  File "/usr/local/lib/python3.10/dist-packages/cfnbootstrap/aws_client.py", line 23, in <module>
    from cfnbootstrap import util, public_constants
  File "/usr/local/lib/python3.10/dist-packages/cfnbootstrap/util.py", line 22, in <module>
    from cfnbootstrap.packages.requests.exceptions import ConnectionError, HTTPError, Timeout, SSLError
  File "/usr/local/lib/python3.10/dist-packages/cfnbootstrap/packages/requests/__init__.py", line 58, in <module>
    from . import utils
  File "/usr/local/lib/python3.10/dist-packages/cfnbootstrap/packages/requests/utils.py", line 30, in <module>
    from .cookies import RequestsCookieJar, cookiejar_from_dict
  File "/usr/local/lib/python3.10/dist-packages/cfnbootstrap/packages/requests/cookies.py", line 159, in <module>
    class RequestsCookieJar(cookielib.CookieJar, collections.MutableMapping):
AttributeError: module 'collections' has no attribute 'MutableMapping'
```
