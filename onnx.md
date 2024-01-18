> onnx





# exporting openNMT to ONNX
python -m tf2onnx.convert --saved-model /home/azureuser/cloudfiles/code/toy-ende_lite/ --output dst/path/model.onnx --opset 13
fail, error : 
2024-01-14 16:35:24,876 - ERROR - rewriter <function rewrite_single_direction_lstm at 0x7fe2828c2f70>: exception graph input 'length' not exist

potential fix ?
python -m tf2onnx.convert --input detection.pb --inputs input_images:0 --outputs feature_fusion/Conv_7/Sigmoid:0,feature_fusion/concat_3:0 --output ./detection.onnx --opset 8

## openNMT tflite to ONNX
python -m tf2onnx.convert --tflite /home/azureuser/cloudfiles/code/toy-ende_lite/opennmt.tflite --output /home/azureuser/cloudfiles/code/toy-ende_lite/model.onnx --opset 13
=> ValueError: Received a shape scalar with unknown static value.  A static value of '-1' is required to represent an unknown shape.
