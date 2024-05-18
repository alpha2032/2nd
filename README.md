from PIL import Image 
import matplotlib.pyplot as plt   
# Open the images 
img1 = Image.open("shadow.jpg")   
img2 = Image.open("battle.jpg")   
# Paste img2 onto img1 at position (200, 250) 
img1.paste(img2, (200, 250))   
img1.show()   
# Generate and display histogram 
histogram = img1.histogram()   
plt.hist(histogram, bins=len(histogram))   
plt.xlabel("Value") 
plt.ylabel("Frequency") 
plt.title("Histogram") 
plt.show()    
# Transpose img2 
transposed_img = img2.transpose(Image.FLIP_LEFT_RIGHT)   
transposed_img.show() 
# Split img1 into RGB bands and process them 
red, green, blue = img1.split() 
zero = red.point(lambda _: 0) 
red_band = Image.merge("RGB", (red, zero, zero)) 
green_band = Image.merge("RGB", (zero, green, zero)) 
blue_band = Image.merge("RGB", (zero, zero, blue)) 
# Show the RGB bands 
red_band.show() 
green_band.show()   
blue_band.show()   
# Save img1 as a BMP file 
img1.save("new_img.bmp")   
# Create a thumbnail for img2 
MAX_SIZE = (100, 100)   
img2.thumbnail(MAX_SIZE)   
img2.save("thumbnail.png")
