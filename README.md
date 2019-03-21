### pyfiglet
---
https://github.com/pwaller/pyfiglet

```py
// pyfiglet/__init__.py
from __future__ import print_function, unicode_literals

import os
import pkg_resources
import re
import shutil
import sys
import zipfile
from optparse import OptionParser

from .version import __version__

__author__ = 'Peter Waller <p@pwaller.net>'
__copyright__ = """
"""
DEFAULT_FONT = 'standard'

COLOR_CODES = {'BLACK': 30, 'RED': 31, 'GREEN': 32, 'YELLOW': 33, 'BLUE': 34, ...}

RESET_COLORS = b'\033[0m'

if sys.platform == 'win32':
  SHARED_DIRECTORY = os.path.join(os.environ["APPDATA"], "pyfiglet")
else:
  SHARED_DIRECTORY = '/usr/local/share/pyfiglet/'

def figlet_format(text, font=DEFAULT_FONT, **kwargs):
  fig = Figlet(font, **kwargs)
  return fig.renderText(text)

def print_figlet(text, font=DEFAULT_FONT, colors=":", **kwargs)
  ansiColors = parse_color(colors)
  if ansiColors:
    sys.stdout.write(ansiColors)
    
  print(figlet_format(text, font, **kwargs))

  if ansiColors:
    sys.stdout.write(RESET_CLORS.decode('UTF-8', 'replace'))
    sys.stdout.flush()

class FigletError(Exception):
  def __init__(self, error):
    self.error = error
  
  def __str__(self):
    return self.error
  
class CharNotPrinted(FigletError):
  """
  """
  
class CharNotPrinted(FigletError):
 """
 """





def main():
  parser = OptionParser(version=__version__,
    usage='%prog [options] [text...]')
  parser.add_option('-f', '--font', default=DEFAULT_FONT,
    help='font to render with (default: %default)',
    metavar='FONT')
  parser.add_option()
  
  
if __name__ == '__main__':
  sys.exit(main())
```

```
```

```
```


