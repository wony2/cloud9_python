# cloud9_python
python with aws cloud9

# pip upgrade
> sudo pip install -U pip

ec2-user:~/environment $ bash: /usr/bin/pip: No such file or directory
ec2-user:/usr/local/bin $ vi ~/.bashrc
# "export PATH=$PATH:/usr/local/bin" add to lastline

ec2-user:/usr/local/bin $ cd ~
ec2-user:~ $ bash
ec2-user:~ $ echo $PATH

# pip install pymysql
> pip install pymysql
######################################## error ########################################
Collecting pymysql
  Using cached https://files.pythonhosted.org/packages/a7/7d/682c4a7da195a678047c8f1c51bb7682aaedee1dca7547883c3993ca9282/PyMySQL-0.9.2-py2.py3-none-any.whl
Collecting cryptography (from pymysql)
  Using cached https://files.pythonhosted.org/packages/dd/c2/3a5bfefb25690725824ade71e6b65449f0a9f4b29702cce10560f786ebf6/cryptography-2.2.2-cp27-cp27mu-manylinux1_x86_64.whl
Collecting asn1crypto>=0.21.0 (from cryptography->pymysql)
  Using cached https://files.pythonhosted.org/packages/ea/cd/35485615f45f30a510576f1a56d1e0a7ad7bd8ab5ed7cdc600ef7cd06222/asn1crypto-0.24.0-py2.py3-none-any.whl
Collecting cffi>=1.7; platform_python_implementation != "PyPy" (from cryptography->pymysql)
  Using cached https://files.pythonhosted.org/packages/14/dd/3e7a1e1280e7d767bd3fa15791759c91ec19058ebe31217fe66f3e9a8c49/cffi-1.11.5-cp27-cp27mu-manylinux1_x86_64.whl
Requirement already satisfied: enum34; python_version < "3" in /usr/local/lib/python2.7/site-packages (from cryptography->pymysql) (1.1.6)
Requirement already satisfied: six>=1.4.1 in /usr/local/lib/python2.7/site-packages (from cryptography->pymysql) (1.11.0)
Collecting idna>=2.1 (from cryptography->pymysql)
  Using cached https://files.pythonhosted.org/packages/4b/2a/0276479a4b3caeb8a8c1af2f8e4355746a97fab05a372e4a2c6a6b876165/idna-2.7-py2.py3-none-any.whl
Collecting ipaddress; python_version < "3" (from cryptography->pymysql)
  Using cached https://files.pythonhosted.org/packages/fc/d0/7fc3a811e011d4b388be48a0e381db8d990042df54aa4ef4599a31d39853/ipaddress-1.0.22-py2.py3-none-any.whl
Collecting pycparser (from cffi>=1.7; platform_python_implementation != "PyPy"->cryptography->pymysql)
  Using cached https://files.pythonhosted.org/packages/8c/2d/aad7f16146f4197a11f8e91fb81df177adcc2073d36a17b1491fd09df6ed/pycparser-2.18.tar.gz
cloud-init 0.7.6 requires argparse, which is not installed.
cloud-init 0.7.6 requires cheetah, which is not installed.
cloud-init 0.7.6 requires oauth, which is not installed.
cloud-init 0.7.6 requires PrettyTable, which is not installed.
cloud-init 0.7.6 requires pyserial, which is not installed.
Installing collected packages: asn1crypto, pycparser, cffi, idna, ipaddress, cryptography, pymysql
Could not install packages due to an EnvironmentError: [Errno 13] Permission denied: '/usr/lib/python2.7/dist-packages/asn1crypto'
Consider using the `--user` option or check the permissions.

