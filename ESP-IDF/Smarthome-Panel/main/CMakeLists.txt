idf_component_register(
    SRCS main.c
    ui_Screen1.c
    ui.c
    ui_comp_hook.c
    ui_helpers.c
    ui_img_bg_png.c
    ui_img_lamp_png.c
    ui_img_curtain_png.c
    ui_img_1202935209.c
    ui_img_plus_png.c
    ui_img_min_nimum_png.c
    ui_img_light_png.c
    INCLUDE_DIRS .)

idf_component_get_property(LVGL_LIB lvgl__lvgl COMPONENT_LIB)
target_compile_options(
    ${LVGL_LIB} 
    PRIVATE 
        -DLV_LVGL_H_INCLUDE_SIMPLE
        -DLV_USE_DEMO_MUSIC
)
