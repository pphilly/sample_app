# A sample Guardfile
# More info at https://github.com/guard/guard#readme

guard 'spork', :rspec_env => { 'RAILS_ENV' => 'test' } do
  watch('config/application.rb')
  watch('config/environment.rb')
  watch(%r{^config/environments/.+\.rb$})
  watch(%r{^config/initializers/.+\.rb$})
  watch('Gemfile')
  watch('Gemfile.lock')
  watch('spec/spec_helper.rb')
  watch('test/test_helper.rb')
  watch('spec/support/')
end

guard 'rspec', :version => 2, :all_after_pass => false, :cli => '--drb' do
  watch(%r{^spec/.+_spec\.rb$})
  
  watch('config/routes.rb')                           { "spec" }
  watch('app/controllers/application_controller.rb')  { "spec" }
  watch('spec/spec_helper.rb')                        { "spec" }
  watch(%r{^app/(.+)\.rb$})                           { "spec" }
  watch(%r{^app/(.*)(\.erb|\.haml)$})                 { "spec" }
  watch(%r{^app/controllers/(.+)_(controller)\.rb$})  { "spec" }
  watch(%r{^app/views/(.+)/})                         { "spec" }
  watch(%r{^spec/support/(.+)\.rb$})                  { "spec" }  
end



