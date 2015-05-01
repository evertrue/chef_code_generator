# Custom Chef Generator Cookbook

Customised Chef Generator Cookbook for starting your Chef masterpiece.  Gives you a beefed up cookbook with

* Rubocop
* Travis CI
* Gemfile
* editorconfig
* Much better README
* CHANGELOG

and many other goodies

# Requirements

* ChefDK

# Usage

This cookbook is not quite like other cookbooks.

1. Clone this cookbook a folder named **code_generator** ex. `~/dev/code_generator`

  ```
  git clone https://github.com/evertrue/et_chef_generator ~/dev/code_generator
  ```
2. You have the option of specifying which code generator to use each time or to make it your default
  * Specify the generator each time. (pass the parent of the code_generator folder)
  ```
  chef generate cookbook <your cookbook> --generator-cookbook '~/dev' --email="devops@evertrue.com" --copyright "EverTrue, inc."
  ```
  * Always use it. Backup your default chef generator and then link up our generator
  ```
  sudo mv /opt/chefdk/embedded/apps/chef-dk/lib/chef-dk/skeletons/code_generator/ ~/dev/original_code_generator
  sudo ln -s ~/dev/code_generator /opt/chefdk/embedded/apps/chef-dk/lib/chef-dk/skeletons/code_generator
  chef generate cookbook <your cookbook> --email="devops@evertrue.com" --copyright "EverTrue, inc."
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
