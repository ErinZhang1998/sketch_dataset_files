`df_all_category_image_split.csv` contains (sketch, text) pairs.

`angel.ndjson` and `face.ndjson` contains raw sketches, which are sequences of strokes, and each stroke contains a sequence of vectors in the format `(dx,dy,p,l)`. 
1. `dx` displacement of x coordinate compared to previous points
2. `dy` displacement of y coordinate compared to previous points
3. `p` is 1 if the current point is the last point of a stroke.
4. `l` semantic label. 

Read `ndjson` file by `json.load(open('face.ndjson', 'r'))["train_data"][image_idx]` to access the `image_idx`-th sketch in the *face* category.
