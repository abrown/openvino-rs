# MobileNet Test Fixture

In order to test the use of `openvino-rs` in the real world, here we include the necessary files for
performing the classification in [classify-mobilenet.rs](../classify-mobilenet.rs). The artifacts
are included in-tree and can be rebuilt using the [build.sh] script (with the right system
dependencies). The artifacts include:
 - the MobileNet inference model, converted to OpenVINO IR format (`*.bin`, `*.mapping`, `*.xml`)
   using [this
   guide](https://github.com/openvinotoolkit/open_model_zoo/blob/master/models/public/mobilenet-v2-1.0-224/model.yml)
 - an image from the COCO dataset transformed into the correct tensor format (`tensor-*.bgr`)

The [mod.sh] `Fixture` provides the correct artifact paths in Rust.
