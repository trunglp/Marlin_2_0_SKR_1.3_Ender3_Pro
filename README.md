![image](https://user-images.githubusercontent.com/38026441/64304063-32cf7e00-cfb5-11e9-85cd-827efb729e26.png)

# Marlin_2_0_SKR_1.3_Ender3_Pro
Marlin 2.0 for SKR V1.3 Ender 3 Pro

-------------------------------
Cải thiện in USB
#define DEFAULT_MINSEGMENTTIME 50000
#if ENABLED (SDSUPPORT)
  #define BLOCK_BUFFER_SIZE 64 
#else
  #define BLOCK_BUFFER_SIZE 64 
#endif

#define MAX_CMD_SIZE 96
#define BUFSIZE 32
#define TX_BUFFER_SIZE 64

--------------------------------

nghiên cứu mở chổ này
#define S_CURVE_ACCELERATION

#define HOMING_FEEDRATE_Z (4 * 60) // Nếu bạn sử dụng cảm biến mức tự động BLTouch / 3DTouch, bạn có thể tăng giá trị lên (10 * 60) để tăng tốc độ hiệu chỉnh tự động

Chúng tôi thiết lập thêm các dải phân cách tốc độ nhẹ nhàng của người Viking để homing, để đoạn phim giới thiệu ít hơn
#define HOMING_BUMP_DIVISOR {4, 4, 4} // Chia lại số chia tốc độ ( Homing)

--------------
Bật chế độ im lặng StealthChop (trên trục của máy đùn, đặc biệt là với bộ nạp bánh răng, SpreadCycle hoạt động ổn định hơn, theo cảm nhận của tôi)

#define STEALTHCHOP_XY
#define STEALTHCHOP_Z
// # xác định STEALTHCHOP_E  
// Intentionally enabling spreadCycle for E
  
--------------------------
#define E0_AUTO_FAN_PIN P2_04

#define E0_AUTO_FAN_PIN P2_04

#define GRID_MAX_POINTS_X 4 // количество точек измерения
  
Nghiên cứu  
#define POWER_LOSS_RECOVERY
  
#define DEFAULT_AXIS_STEPS_PER_UNIT   {80.000,80.000,400.000,426.67,400.0}  // default steps per unit for Ultimaker
#define DEFAULT_MAX_FEEDRATE          {500, 500, 5, 25}    // (mm/sec)
  
  
  Xem lại 
  #define LIN_ADVANCE
  
  nghiên cứu set E 750
  


##Ender 3 Pro sử dụng 24V
#define CHOPPER_TIMING CHOPPER_DEFAULT_24V
  
  
