# android_touchscreen_msg22xx

implement to dts

&soc {
	i2c@78b9000 { /* BLSP1 QUP5 */
		mstar@26 {
			compatible = "mstar,msg2xxx";
			reg = <0x26>;
			interrupt-parent = <&msm_gpio>;
			interrupts = <13 0x2>;
			vdd-supply = <&pm8909_l17>;
			vcc_i2c-supply = <&pm8909_l6>;
			mstar,family-id = <0x2>;
			mstar,reset-gpio = <&msm_gpio 12 0x0>;
			mstar,irq-gpio = <&msm_gpio 13 0x0>;
			mstar,display-coords = <0 0 480 854>;
			mstar,panel-coords = <0 0 480 854>;
			mstar,button-map = <172 139 158>;
			mstar,no-force-update;
			mstar,i2c-pull-up;
		};
	};
};
