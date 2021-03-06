
set( TRICKMATH_SRC
  src/LUD_inv
  src/LUT_inv
  src/LU_bksb
  src/LU_dcmp
  src/RodriguesRotation
  src/dLU_Choleski
  src/dLU_solver
  src/dS_function
  src/deuler_123
  src/deuler_123_quat
  src/deuler_132
  src/deuler_132_quat
  src/deuler_213
  src/deuler_213_quat
  src/deuler_231
  src/deuler_231_quat
  src/deuler_312
  src/deuler_312_quat
  src/deuler_321
  src/deuler_321_quat
  src/dm_add
  src/dm_copy
  src/dm_ident
  src/dm_init
  src/dm_invert
  src/dm_invert_symm
  src/dm_orthonormal
  src/dm_print
  src/dm_scale
  src/dm_sub
  src/dm_trans
  src/dmtxm
  src/dmtxmt
  src/dmtxv
  src/dmxm
  src/dmxmt
  src/dmxv
  src/drandom_gaussian
  src/dsingle_axis_rot
  src/dv_add
  src/dv_copy
  src/dv_cross
  src/dv_dot
  src/dv_init
  src/dv_mag
  src/dv_norm
  src/dv_print
  src/dv_scale
  src/dv_skew
  src/dv_store
  src/dv_sub
  src/dvxm
  src/dvxv_add
  src/dvxv_sub
  src/eigen_hh_red
  src/eigen_jacobi
  src/eigen_jacobi_4
  src/eigen_ql
  src/euler_matrix
  src/euler_quat
  src/gauss_rnd_bell
  src/gauss_rnd_pseudo
  src/mat_copy
  src/mat_permute
  src/mat_print
  src/mat_to_quat
  src/mat_trans
  src/matxmat
  src/matxtrans
  src/matxvec
  src/quat_mult
  src/quat_norm
  src/quat_norm_integ
  src/quat_to_mat
  src/rand_num
  src/roundoff
  src/tm_print_error
  src/transxmat
  src/transxtrans
  src/transxvec
  src/trick_gsl_rand
  src/trns_fnct_1o
  src/trns_fnct_2o
  src/uniform_rnd_1
  src/uniform_rnd_triple
  src/vec_print
  src/wave_form
)

add_library( trick_math STATIC ${TRICKMATH_SRC})

if(GSL_FOUND)
    target_include_directories( trick_math PUBLIC ${GSL_INCLUDE_DIRS} )
endif()
