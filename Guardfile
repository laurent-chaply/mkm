guard 'livereload' do
  watch('rspec.html')
  watch('coverage/index.html')
end
guard :rspec, cmd: 'bundle exec rspec', all_after_pass: true do
  watch(%r{^spec/.+_spec\.rb$})
  watch(%r{^lib/(.+)\.rb$})     { |m| "spec/#{m[1]}_spec.rb" }
  watch('spec/spec_helper.rb')  { "spec" }
end
