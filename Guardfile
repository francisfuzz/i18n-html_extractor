# frozen_string_literal: true

guard :rubocop, cli: '--auto-correct --display-cop-names' do
  watch(/.+\.rb$/)
  watch(%r{(?:.+/)?\.rubocop.*\.yml$}) { |m| File.dirname(m[0]) }
end

guard :rspec, cmd: 'bundle exec rspec' do
  watch(/^.+_spec\.rb$/)
  watch(%r{^spec/.+_spec\.rb$})
  watch(%r{^lib/(.+)\.rb}) { |m| "spec/lib/#{m[1]}_spec.rb" }
  watch('spec/spec_helper.rb') { 'spec' }
end
