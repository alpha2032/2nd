# 2nd
classes and object
class Television  
attr_accessor :brand, :model, :screen_size, :volume  
def initialize(brand, model, screen_size)  
@brand = brand  
@model = model  
@screen_size = screen_size  
@volume = 50  
end  
def turn_on  
puts "#{@brand} TV is now turned on."  
end  
def change_channel(channel)  
puts "#{@brand} TV is now tuned to channel #{channel}."  
end  
def adjust_volume(volume)  
@volume += volume  
puts "#{@brand} TV volume adjusted to #{@volume}."  
end  
end  
class Speaker  
attr_accessor :brand, :model, :volume  
def initialize(brand, model)  
@brand = brand  
@model = model  
@volume = 50  
end  
def turn_on  
puts "#{@brand} speakers are now turned on."  
end  
def play_music  
puts "#{@brand} speakers are playing music."  
end  
def adjust_volume(volume)  
@volume += volume  
puts "#{@brand} speakers volume adjusted to #{@volume}."  
end  
end  
tv = Television.new("LG", "Bravia", 55)  
tv.turn_on  
tv.change_channel(7)  
tv.adjust_volume(10)  
speaker = Speaker.new("BOAT", "SoundLink")  
speaker.turn_on  
speaker.play_music  
speaker.adjust_volume(5) 
