# mcollective modulepackager template

The mcollective package modulepackager target added in MCollective 2.3.3
renders a directory of templates to create the module metadata for the package.

Any file in that templates directory ending .erb and not starting with an
underscore will be expanded with ERB.

The \_manifest.pp.erb is a template that will be used to generate the specific
mcollective\_plugin\_foo::agent mcollective\_plugin\_foo::application class
templates.


    $ cd my-awesome-plugin
    $ mco plugin package \
        --format modulepackage \
        --vendor richardc \
        --module-template ~/src/my_special_template
