# android_touchscreen_msg22xx

implement to dts

&soc {
	i2c@78b9000 { /* BLSP1 QUP5 */
		mstar@26{
			compatible = "mstar,msg2xxx";
			reg = <0x26>;
			pinctrl-names = "pmx_ts_int_active","pmx_ts_int_suspend"; 
			pinctrl-0 = <&ts_int_active>; 
			pinctrl-1 = <&ts_int_suspend>;
			interrupt-parent = <&msm_gpio>;
			interrupts = <13 0x2008>;
			vdd-supply = <&pm8909_l17>;
			vcc_i2c-supply = <&pm8909_l6>;

			mstar,name = "msg2xxx";			
			mstar,reset-gpios = <&msm_gpio 12 0x0>;
			mstar,interrupt-gpios = <&msm_gpio 13 0x2008>;	
			mstar,panel-coords = <0 0 480 954>;
			mstar,display-coords = <0 0 480 854>;
			mstar,button-map= <158 172 139>;
			mstar,no-force-update;
			mstar,i2c-pull-up;
			mstar,family-id = <0x0>;	

			mstar,disp-maxx = <480>;
			mstar,disp-maxy = <854>;
			mstar,pan-maxx = <480>;
			mstar,pan-maxy = <954>;
			mstar,key-codes = <158 172 139>;
			mstar,y-offset = <0>;
		};
	};
};
