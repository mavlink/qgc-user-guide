# Motor Kurulumu

Motor Kurulumu, ayrı motorları / servoları test etmek için kullanılır (örneğin, motorların doğru yönde döndüğünü doğrulamak için).

> **Tip** Bu talimatlar PX4 ve ArduPilot'taki çoğu araç türü için geçerlidir. Araca özel talimatlar, alt konular olarak sağlanır (örn. [ Motor Kurulumu (ArduSub) ](../SetupView/Motors_ardusub.md)).

![Motors Test](../../assets/setup/Motors.png)

## Test Adımları

Motorları test etmek için:

1. Tüm pervaneleri çıkarın. > **Warning** You must remove props before activating the motors!
2. (*PX4-only*) Enable safety switch - if used.
3. Slide the switch to enable motor sliders (labeled: *Propellers are removed - Enable motor sliders*).
4. Adjust the individual sliders to spin the motors and confirm they spin in the correct direction. > **Note** The motors only spin after you release the slider and will automatically stop spinning after 3 seconds.

## Additional Information

- [Basic Configuration > Motor Setup](http://docs.px4.io/master/en/config/motors.html) (*PX4 User Guide*) - This contains additional PX4-specific information.