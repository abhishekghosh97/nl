import ipywidgets as widgets
from IPython.display import display, Image

# Define functions to display images and info
def display_entry(image_path, info1, info2):
    image = Image(filename=image_path, width=200, height=200)
    output = widgets.Output()
    with output:
        display(image)
    entry_layout = widgets.Layout(border="2px solid black", padding="5px", margin="10px")  # Added margin
    return widgets.VBox([output, widgets.HTML(value=f"<b>{info1}</b><br>{info2}")], layout=entry_layout)

# Define dashboard entries
entries = [
    {"image": "nl.png", "info1": "Evaluations done yesterday:26 ", "info2": "10 day average:31 "},
    {"image": "nl.png", "info1": "Evaluations done yesterday:45 ", "info2": "10 day average:47 "},
    {"image": "nl.png", "info1": "Evaluations done yesterday:0 ", "info2": "10 day average:14 "},
    {"image": "nl.png", "info1": "Evaluations done yesterday:33 ", "info2": "10 day average:13 "}
]

# Display entries in a grid layout
grid_entries = []
for entry in entries:
    image_path = entry["image"]
    info1 = entry["info1"]
    info2 = entry["info2"]
    grid_entries.append(display_entry(image_path, info1, info2))

# Arrange entries in a 2x2 grid
rows = []
for i in range(0, len(grid_entries), 2):
    row_entries = grid_entries[i:i+2]
    rows.append(widgets.HBox(row_entries, layout=widgets.Layout(margin="10px")))  # Added margin

# Display grid
display(widgets.VBox(rows, layout=widgets.Layout(margin="10px")))

