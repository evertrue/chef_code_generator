# et_chef_generator

Customised Chef Generator Cookbook for starting your Chef masterpiece 

# Requirements

* ChefDK

# Usage

This cookbook is not quite like other cookbooks.

1. Clone this cookbook to some folder named code_generator `~/dev/code_generator`
  * `git clone https://github.com/evertrue/et_chef_generator ~/dev/code_generator`
2. You have the option of specifying which code generator to use each time or to make it your default
  * Specify each time: `chef generate cookbook <your cookbook> --generator-cookbook '~/dev'`
  * Make Default: Backup your default chef generator and then clone our generator to it
    * mv /opt/chefdk/embedded/lib/ruby/gems/2.1.0/gems/chef-dk-0.4.0/lib/chef-dk/skeletons/code_generator/ ~/dev/original_code_generator
    * ln -s /opt/chefdk/embedded/lib/ruby/gems/2.1.0/gems/chef-dk-0.4.0/lib/chef-dk/skeletons/code_generator/ ~/dev/code_generatore
    
## Contributing

1. Fork the repository on Github
2. Create a named feature branch (like `add_component_x`)
3. Write your change
4. Write tests for your change (if applicable)
5. Run the tests with `kitchen test`, ensuring they all pass
6. Submit a Pull Request using Github

## License and Authors

Author:: EverTrue, inc. (devops@evertrue.com)
