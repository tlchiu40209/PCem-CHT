pcem_private_api += files(
        '../../includes/private/video/video.h',
        '../../includes/private/video/vid_et4000.h',
        '../../includes/private/video/vid_et4000w32.h',
        '../../includes/private/video/vid_genius.h',
        '../../includes/private/video/vid_hercules.h',
        '../../includes/private/video/vid_ht216.h',
        '../../includes/private/video/vid_icd2061.h',
        '../../includes/private/video/vid_ics2595.h',
        '../../includes/private/video/vid_im1024.h',
        '../../includes/private/video/vid_incolor.h',
        '../../includes/private/video/vid_mda.h',
        '../../includes/private/video/vid_mga.h',
        '../../includes/private/video/vid_olivetti_m24.h',
        '../../includes/private/video/vid_oti037.h',
        '../../includes/private/video/vid_oti067.h',
        '../../includes/private/video/vid_paradise.h',
        '../../includes/private/video/vid_pc1512.h',
        '../../includes/private/video/vid_pc1640.h',
        '../../includes/private/video/vid_pc200.h',
        '../../includes/private/video/vid_pcjr.h',
        '../../includes/private/video/vid_pgc.h',
        '../../includes/private/video/vid_ps1_svga.h',
        '../../includes/private/video/vid_s3.h',
        '../../includes/private/video/vid_s3_virge.h',
        '../../includes/private/video/vid_sdac_ramdac.h',
        '../../includes/private/video/vid_sigma.h',
        '../../includes/private/video/vid_stg_ramdac.h',
        '../../includes/private/video/vid_svga.h',
        '../../includes/private/video/vid_svga_render.h',
        '../../includes/private/video/vid_svga_render_remap.h',
        '../../includes/private/video/vid_t1000.h',
        '../../includes/private/video/vid_t3100e.h',
        '../../includes/private/video/vid_tandy.h',
        '../../includes/private/video/vid_tandysl.h',
        '../../includes/private/video/vid_tgui9440.h',
        '../../includes/private/video/vid_tkd8001_ramdac.h',
        '../../includes/private/video/vid_tvga.h',
        '../../includes/private/video/vid_tvp3026_ramdac.h',
        '../../includes/private/video/vid_unk_ramdac.h',
        '../../includes/private/video/vid_vga.h',
        '../../includes/private/video/vid_voodoo_banshee_blitter.h',
        '../../includes/private/video/vid_voodoo_banshee.h',
        '../../includes/private/video/vid_voodoo_blitter.h',
        '../../includes/private/video/vid_voodoo_codegen_x86-64.h',
        '../../includes/private/video/vid_voodoo_codegen_x86.h',
        '../../includes/private/video/vid_voodoo_common.h',
        '../../includes/private/video/vid_voodoo_display.h',
        '../../includes/private/video/vid_voodoo_dither.h',
        '../../includes/private/video/vid_voodoo_fb.h',
        '../../includes/private/video/vid_voodoo_fifo.h',
        '../../includes/private/video/vid_voodoo.h',
        '../../includes/private/video/vid_voodoo_reg.h',
        '../../includes/private/video/vid_voodoo_regs.h',
        '../../includes/private/video/vid_voodoo_render.h',
        '../../includes/private/video/vid_voodoo_setup.h',
        '../../includes/private/video/vid_voodoo_texture.h',
        '../../includes/private/video/vid_wy700.h',
        '../../includes/private/video/vid_ati18800.h',
        '../../includes/private/video/vid_ati28800.h',
        '../../includes/private/video/vid_ati68860_ramdac.h',
        '../../includes/private/video/vid_ati_eeprom.h',
        '../../includes/private/video/vid_ati_mach64.h',
        '../../includes/private/video/vid_cga.h',
        '../../includes/private/video/vid_cl5429.h',
        '../../includes/private/video/vid_colorplus.h',
        '../../includes/private/video/vid_compaq_cga.h',
        '../../includes/private/video/vid_ddc.h',
        '../../includes/private/video/vid_ega.h'
        )

if get_option('allow-experimental-code') and get_option('use-experimental-pdc')
        add_project_arguments('-DUSE_EXPERIMENTAL_PGC', language: ['c', 'cpp'])
endif

pcem_src += files(
        'vid_ati18800.c',
        'vid_ati28800.c',
        'vid_ati68860_ramdac.c',
        'vid_ati_eeprom.c',
        'vid_ati_mach64.c',
        'vid_cga.c',
        'vid_cl5429.c',
        'vid_colorplus.c',
        'vid_compaq_cga.c',
        'vid_ddc.c',
        'vid_ega.c',
        'vid_et4000.c',
        'vid_et4000w32.c',
        'vid_genius.c',
        'vid_hercules.c',
        'vid_ht216.c',
        'vid_icd2061.c',
        'vid_ics2595.c',
        'vid_im1024.c',
        'vid_incolor.c',
        'vid_mda.c',
        'vid_mga.c',
        'vid_olivetti_m24.c',
        'vid_oti037.c',
        'vid_oti067.c',
        'vid_paradise.c',
        'vid_pc1512.c',
        'vid_pc1640.c',
        'vid_pc200.c',
        'vid_pcjr.c',
        'vid_pgc.c',
        'vid_ps1_svga.c',
        'vid_s3.c',
        'vid_s3_virge.c',
        'vid_sdac_ramdac.c',
        'vid_sigma.c',
        'vid_stg_ramdac.c',
        'vid_svga.c',
        'vid_svga_render.c',
        'vid_t1000.c',
        'vid_t3100e.c',
        'vid_tandy.c',
        'vid_tandysl.c',
        'vid_tgui9440.c',
        'vid_tkd8001_ramdac.c',
        'vid_tvga.c',
        'vid_tvp3026_ramdac.c',
        'vid_unk_ramdac.c',
        'vid_vga.c',
        'vid_voodoo.c',
        'vid_voodoo_banshee.c',
        'vid_voodoo_banshee_blitter.c',
        'vid_voodoo_blitter.c',
        'vid_voodoo_display.c',
        'vid_voodoo_fb.c',
        'vid_voodoo_fifo.c',
        'vid_voodoo_reg.c',
        'vid_voodoo_render.c',
        'vid_voodoo_setup.c',
        'vid_voodoo_texture.c',
        'vid_wy700.c',
        'video.c'
        )