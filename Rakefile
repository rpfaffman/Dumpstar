require './app'
require 'sinatra/activerecord/rake'
require 'gnip-stream'

desc 'open GNIP stream'
task :stream do
  twitter_stream = GnipStream::PowertrackClient.new(ENV['GNIP_URL'], ENV['GNIP_USERNAME'], ENV['GNIP_PASSWORD'])
  twitter_stream.consume { |message| puts message }
end