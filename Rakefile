namespace :posts do
  desc "Create a new post, you can specify the title with new[Title goes here]"
  task :new, [:name] do |t, args|
    time = Time.now
    name = args[:name] || "New Post"
    filename = format("%4d-%02d-%02d-%s.md", time.year, time.month, time.day, name.downcase.gsub(/\s+/, '_'))
    open File.join("_posts", filename), "w+" do |io|
      io.puts "---"
      io.puts "title: #{name}"
      io.puts "layout: default"
      io.puts "---"
      io.puts "\nWrite your post here :)"
    end
    puts "New post created: #{filename}"
  end
end