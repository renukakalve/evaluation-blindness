1) Why is CIFAR-10 accuracy easy to optimize?
My Ans:- Because CIFAR-10 images are small, clean, and very similar to each other.
In CIFAR-10 the training and test data/images come from the same conditions like small,
clean images & same type etc, that's why models depends on colors, textures or background
patterns. Because benchmark never tests different real world conditions like blur ,noisy and
different background images, the model is not forced to learn truly meaningful or stable features.
As a result, models can get high accuracy without really understanding the objects.
  	
2) Why does CIFAR-10 NOT represent real-world vision?
My Ans:- Real-world vision systems face many changes like different size image, background, camera quality,
blur and noisy image, and different environments. CIFAR-10 does not satisfy these variations and instead uses
very clean and similar/controlled images. Because of this, models tested on CIFAR-10 are never checked on the
basis of real world challenges. As a result, CIFAR-10 does not satisfy show how well a model will work in real-
world situations.

Note:- Models perform very well on clean benchmarks like CIFAR-10, but their performance drops when small, realistic 
changes are occurred, such as noise or blur image in CIFAR-10-C. This shows that standard evaluation methods do not 
reveal when models dependon shorcuts, and they can give false sense of reliability for real world use.

Predictions(Expected Failure):- I expect the model's accuracy to drop a lot when noise or blur is added to the images. 
Even when the predictions are wrong, the madel may still be very confident about its answers. Becauese the benchmark 
only checks accuracy on clean images, it will not give any warning that the model is unreliable in real-worls conditions.

