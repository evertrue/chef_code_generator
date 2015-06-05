# Custom Chef Generator Cookbook

Customised Chef Generator Cookbook for starting your Chef masterpiece.  Gives you a beefed up cookbook with

* Rubocop
* Travis CI
* Gemfile
* editorconfig
* Much better README
* CHANGELOG

and many other goodies

Disclaimer: This generator is slightly opinionated towards our style and process at EverTrue, however 
it should be a good example of how to make your own generator cookbook.

# Requirements

* ChefDK

# Usage

This cookbook is not quite like other cookbooks.  Note that you can replace `~/dev` with anything you like

1. Clone this cookbook a folder named **code_generator** ex. `~/dev/code_generator`

  ```bash
  git clone https://github.com/evertrue/et_chef_generator ~/dev/code_generator
  ```
2. You have the option of specifying a generator manually or set ours as the default
  * Specify the generator every time you generate a cookbook. (pass the parent of the `code_generator` folder)
  ```bash
  chef generate cookbook <your cookbook> --generator-cookbook '~/dev' --email="<Maintainer Email>" --copyright "<Your Org>" -l <License>
  ```
  * Always use it. Backup your default chef generator and then link to our generator
  ```bash
  # Backup the old generator
  sudo mv /opt/chefdk/embedded/apps/chef-dk/lib/chef-dk/skeletons/code_generator/ ~/dev/original_code_generator
  
  # Symlink the place where chef looks for a code_generator by default to ours in `~/dev`
  sudo ln -s ~/dev/code_generator /opt/chefdk/embedded/apps/chef-dk/lib/chef-dk/skeletons/code_generator

  # Generate cookbooks like so
  chef generate cookbook <your cookbook> --email="<Maintainer Email>" --copyright "<Your Org>" -l <License>
  ```



## Contributing

1. Fork the repository on Github
2. Create a named feature branch (like `add_component_x`)
3. Write your change
4. Write tests for your change (if applicable)
5. Run the tests with `kitchen test`, ensuring they all pass
6. Submit a Pull Request using Github

## License and Authors

Author:: EverTrue, inc. (devops@evertrue.com)
