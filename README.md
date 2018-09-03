This is a sample project that integrates React in a middleman site.

Required files for new middleman-react projects:
* .babelrc
* config.ru?
* gulpfile.js
* package.json (optional: package-lock.json)

To be edited:
* package.json: set project name and description, edit packages required, set git repo
* config.rb: include the following configuration to activate Middleman's external pipeline
<pre>
activate :external_pipeline,
   name: :gulp,
   command: './node_modules/gulp/bin/gulp.js default',
   source: 'dist'
</pre> 
* layout.erb: include all.js where we first initialize the main react component. 
Needs to be included in all layout files where React is required. We might want 
to split this file depending on the project's scope.