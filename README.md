# About-us-code

# Create about_us_tab
about_us_tab = ttk.Frame(notebook)
notebook.add(about_us_tab, text="About ScanSense")

# Create a frame for the content and photo in the "About ScanSense" tab
about_content_frame = tk.Frame(about_us_tab)
about_content_frame.pack(pady=20)

# Add an image
about_image = Image.open("logo.png")
about_image = about_image.resize((150, 150), Image.LANCZOS)
about_photo = ImageTk.PhotoImage(about_image)
label = Label(about_content_frame, image=about_photo, text="""
Developed by: 
Ala’a Almajali
Aya Alshobaki 
Rahaf Albojoq
Sarah Alrashed 
Salsabeel Mousa
""", compound=tk.RIGHT, font=("Arial", 14), anchor='w')
label.image = about_photo
label.pack(pady=10)


# Create a big text box
text_box = Message(about_content_frame, width=780, text="""
Welcome to ScanSense!

ScanSense is a powerful Python-based port scanning and attack detection tool, 
designed to assist network administrators and security professionals
in detecting malicious activities within a network. It employs port scanning and attack detection, 
utilizing the Scapy library to identify open ports and determine associated services. 
ScanSense also utilizes a machine learning model for enhanced attack detection 
and offers network scanning functionality to identify active hosts with automation and real-time updates.
ScanSense ensures efficient and user-friendly scanning processes.""", pady=1) 

text_box.config(font=("Arial", 14))
# Center the text
text_box.pack()

# Load the photo for the about_us_tab
about_photo = Image.open("logo.png")
about_photo = about_photo.resize((900, 900), Image.LANCZOS)
about_photo_image = ImageTk.PhotoImage(about_photo)

root.mainloop()
