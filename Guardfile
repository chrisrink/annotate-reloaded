# A sample Guardfile
# More info at https://github.com/guard/guard#readme


guard 'jshint-node', :config => 'jshint-config.json' do
    watch(%r{^src/main/webapp/annotate/.*\.js$})
end

guard 'remote-sync',
    :source => "./src/main/webapp/annotate/", 
    :destination => "/usr/local/apache-tomcat/6.0.32/webapps/annotate/annotate", 
    :user => 'root',
    :remote_address => 'my.veevavault.com',
    :remote_port => 2222,
    :verbose => true, 
    :cli => "--color" do
   watch(%r{^.+\.(js|css|html|xml|php|png|jspx)$})
end



guard 'livereload' do
	watch(%r{^.+\.(js|css|html|xml|php|png|jspx)$})
end

