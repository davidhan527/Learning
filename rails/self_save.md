1. Process objects should not save themselves because:
  * It ties persistence logic to process object. 
    * This means that we will have to load an active record database when we want to unit test our process object.
