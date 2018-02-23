# CFEngine Beautifier

CFEngine configuration file beautifier written in Python.

- Command line interface
- Integrates with Sublime Text 2 and Sublime Text 3.
- Installation for Sublime by cloning into Sublime Text's Packages folder.

### Sublime Text Installation

#### Via Package Manager

1. Ctrl + Shift + p (Linux, Windows) or Cmd + Shift + p (OS X).
2. Type "install package"
3. Type "cfenginebeautifier"
4. Enter

For more information: https://sublime.wbond.net/docs/usage

#### Manual Installation

1. Navigate to Sublime Text Packages Directory

  <table>
    <tr>
      <th>Platform</th>
      <th>Sublime Text 2</th>
      <th>Sublime Text 3</th>
    </tr>
    <tr>
      <td>Linux</td>
      <td>~/.config/sublime-text-2/Packages</td>
      <td>~/.config/sublime-text-3/Packages</td>
    </tr>
    <tr>
      <td>OS X</td>
      <td>~/Library/Application Support/Sublime Text 2/Packages</td>
      <td>~/Library/Application Support/Sublime Text 3/Packages</td>
    </tr>
    <tr>
      <td>Windows</td>
      <td>%APPDATA%\Sublime Text 2/Packages</td>
      <td>%APPDATA%\Sublime Text 3/Packages</td>
    </tr>
  </table>
  - More information: http://sublimetext.info/docs/en/basic_concepts.html

2. git clone https://github.com/naksu/cfengine_beautifier.git

### Sublime Text Options

<table>
  <tr>
    <th>Option</th>
    <th>Description</th>
    <th>Value</th>
    <th>Default</th>
  </tr>
  <tr>
    <td>beautify_on_save</td>
    <td>Run beautifier every time the file is saved</td>
    <td>true | false</td>
    <td>true</td>
  </tr>
  <tr>
    <td>page_width</td>
    <td>Tries to make text fit onto this width (number of characters)</td>
    <td>number</td>
    <td>100</td>
  </tr>
  <tr>
    <td>remove_empty_promise_types</td>
    <td>Remove promise types (such as vars:, reports:) which have no promises or comments</td>
    <td>true | false</td>
    <td>true</td>
  </tr>
  <tr>
    <td>sort_promise_types_to_evaluation_order</td>
    <td>Sort promise types to CFEngine normal order</td>
    <td>true | false</td>
    <td>true</td>
  </tr>
</table>

### Command Line Options

Run cf-beautify --help

## Building a package with epm

To build a Debian package use the following command:
```sudo epm -v -f deb --output-dir /var/tmp cf-beautifier```
This will use the equal named list `cf-beautifier.list` for building the package.
If you want to use your own list simply append for example `mylist.list` to the command.
