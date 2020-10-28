

## Quick notes
* Cmd line args are passed as strings to a program


### Output format
In node, using process.argv, args start from 'node' so the fun starts from process.argv[2]. So output of `node [program] [one two three]`:
  ```
  0 -> /home/vagrant/.nvm/versions/node/v10.20.1/bin/node
  1 -> /vagrant/w1/d1-focal/processargv.js
  2 -> one
  3 -> two
  4 -> three
  ```
