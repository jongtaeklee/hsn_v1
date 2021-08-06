## HSN jupyter notebook demo 활용 KNUH WSI 결과 확인
- demo_01_segment_patches notebook 에서
  - file I/O 부분 확인
    - ground truth 없는 버전으로 
      - hsn.load_gt() 안 하기
      - gt_mode': 'off'
    - Image load
      - patch file을 KNUH WSI 샘플 이미지에서 224x224 png 파일로 저장해서 폴더에 넣어두기
        - SVS IO work3 을 통해 patch file을 만듬
        - demo_01_segment_patches-gpu-work3 여기서 성능을 확인해 보았으나 성능 미비
        - level 2, 448x448 을 224x224 로 resize 해서 영상 만듬
      - 또는 wsi file 에서 direct로 batch image 제공하기