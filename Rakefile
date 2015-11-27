desc 'create a new draft post'

require 'date'

task :tester do

  print ENV['title']
end


task :post do

    title = ENV['title']
      slug = "#{Date.today}-#{title.downcase.gsub(/[^\w]+/, '-')}"
       uhrzeit = "#{DateTime.now.strftime('%H:%M:%S')}"
       jahr = "#{DateTime.now.strftime('%Y-%m-%d')}"
        file = File.join(
	      File.dirname(__FILE__),
	          '_posts',
		      slug + '.md'
		        )

	  File.open(file, "w") do |f|
	        f << <<-EOS.gsub(/^    /, '')
    ---
    layout: post
    title: #{title}
    categories:
    date: #{jahr} #{uhrzeit}
    ---

    EOS
      end
	  
end
