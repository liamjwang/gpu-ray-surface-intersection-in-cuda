cmake_minimum_required(VERSION 3.25)
project(gpu_ray_surface_intersection_in_cuda)

set(CMAKE_CXX_STANDARD 14)

include_directories(.)
include_directories(scratch)

add_executable(gpu_ray_surface_intersection_in_cuda
        pycuda/pycuda_source.cu
        scratch/bvh_structure.h
        scratch/gpu_ray_surface_intersect.cu
        scratch/gpu_ray_surface_intersect_v1.cu
        scratch/gpu_ray_surface_intersect_v2.cu
        scratch/morton3D.h
        scratch/rsi_geometry.h
        scratch/sort_rays.cu
        bvh_structure.h
        gpu_ray_surface_intersect.cu
        gpu_ray_surface_intersect_v1.cu
        gpu_ray_surface_intersect_v2.cu
        morton3D.h
        rsi_geometry.h
        sort_rays.cu)
