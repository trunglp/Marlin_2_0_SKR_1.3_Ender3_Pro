![image](https://user-images.githubusercontent.com/38026441/64304063-32cf7e00-cfb5-11e9-85cd-827efb729e26.png)

![SKR1 3](https://user-images.githubusercontent.com/38026441/64603378-847b6c80-d3ea-11e9-9a2b-126b74639f10.jpg)

![2019-08-20_16-13-17](https://user-images.githubusercontent.com/38026441/65943606-0a269100-e45a-11e9-938f-d2062ed524a4.png)

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


Firmware is set for low noise prints with highest possible quality.

     
    COM BOUDRATE 1000000
     
    Extruder 1
     
    DEFAULT_NOMINAL_FILAMENT_DIA 1.75
     
    TEMSENSORS SET AS ORIGINAL
     
    PID CALIBRATED TO ORIGINAL HEAD
    DEFAULT_Kp 17.20
    DEFAULT_Ki 1.06
    DEFAULT_Kd 69.58
     
    Prevent Cold Extrusion 190 C
     
    Thermal Protection: Hotends, Bed,
     
    Drivers TMC2208 UART MODE
     
    Steps sets for quality,
     
    BLTouch if used added delay for lower errors,
     
    Probe (BLTouch) position offset set to Minimalistic fan mount - REDESIGN v 4.0
     
    Z SAFE HOMING - 5 mm
     
    BED SIZE = 235 X,Y Z = 250
     
    MESH BED LEVELING - MANUAL OR AUTOMATIC BLTouch,
     
    DEBUG LEVELING ENABLED,
     
    G26 MESH VALIDATION ENABLED,
     
    LCD BED LEVELING ENABLED,
     
    SAFE MANUAL BED LEVELING CORNERS SETS 35 mm FROM EDGE,
     
    EEPROM SETTINGS - M500 ENABLED,
     
    EEPROM CHITCHAT ENABLED,
     
    PREHEAT SET FOR PLA - 215C/50C & PET-G 240C/70C
     
    NOZZLE PARK FEATURE SET,
     
    NOZZLE CLEAN FEATURE G12 ENABLED,
     
    PRINT JOBS STATISTICS ENABLED,
     
    LANGUAGE - EN
     
    SDSUPPORT ENABLED,
     
    INDIVIDUAL AXIS HOMING MENU ENABLED,
     
    CR10 STOCK DISPLAY ENABLED - Stock display for Ender,
     
    ADAPTIVE STEP SMOOTHING,
     
    MICROSTEPS 16
     
    STATUS FAN FRAMES 4,
     
    BABYSTEPPING,
     
    LIN_ADVANCE_K 0.0,
     
    ARC_SUPPORT ,
     
    SERIAL OVERRUN PROTECTION,
     
    ADVANCED_PAUSE_FEATURE - ENABLED,
     
    FILAMENT CHANGE LCD - ENABLED,
     
    TMC2208 CURRENT X,Y,Z - 800, E0 900,
     
    STEALTHCHOP X,Y,Z,E
     
    CHOPPER_TIMING CHOPPER_DEFAULT_24V,
     
    MONITOR_DRIVER_STATUS - M122, M911, M912, M906,
     
    HYBRID_THRESHOLD - DISABLED FOR QUIETLY PRINTS,
     
    TMC DEBUG - ENABLED.
    
    
  
