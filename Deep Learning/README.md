There are two ways of composing models in Keras. They are as follows:
- Sequential composition - Different predefined models are stacked together in a linear pipeline of layers similar to a stack or a queue.
- Functional composition - Here it is possible to define complex models, such as directed acyclic graphs, models with shared layers, or multi-output models.

Saving and loading model architectures:
# save as JSON 
    json_string = model.to_json()
# save as YAML 
    yaml_string = model.to_yaml()
# model reconstruction from JSON: 
    from keras.models import model_from_json 
    model = model_from_json(json_string)
    
    
# Saving parameters (weights):
    from keras.models import load_model 
    model.save('my_model.h5') # creates a HDF5 file 'my_model.h5' 
    
    del model     # deletes the existing model
