# test

<table>
  <thead>
    <tr>
      <th colspan="3">ROS (PointCloud2)</th>
      <th colspan="3">SDR (range)</th>
    </tr>
    <tr>
      <th>필드</th>
      <th>데이터 타입</th>
      <th>설명</th>
      <th>필드</th>
      <th>데이터 타입</th>
      <th>설명 (XROS2 사용)</th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>header</td>
      <td></td>
      <td>time(sec, nsec) + frame_id</td>
      <td style="background:#f8d7da;">time</td>
      <td style="background:#f8d7da;">string</td>
      <td style="background:#f8d7da;">sec + . + nsec 로 변환</td>
    </tr>

    <tr>
      <td>height</td>
      <td>uint32</td>
      <td>기기 마다 다른 고정값, 1채널</td>
      <td></td>
      <td></td>
      <td>임의로 1 지정</td>
    </tr>

    <tr>
      <td>width</td>
      <td>uint32</td>
      <td>기기 마다 다른 고정값, 채널 개수</td>
      <td></td>
      <td></td>
      <td>1회전에 생산되는 포인트 개수</td>
    </tr>

    <tr>
      <td>fields</td>
      <td></td>
      <td>x, y, z 등의 위치와 데이터 정의</td>
      <td></td>
      <td></td>
      <td></td>
    </tr>

    <tr>
      <td>point_step</td>
      <td>uint32</td>
      <td>1 point의 byte</td>
      <td></td>
      <td></td>
      <td>1 point의 byte</td>
    </tr>

    <tr>
      <td>row_step</td>
      <td>uint32</td>
      <td>point_step × width</td>
      <td></td>
      <td></td>
      <td>point_step × width</td>
    </tr>

    <tr>
      <td rowspan="5">data</td>
      <td rowspan="5">uint8[]</td>
      <td rowspan="5">fields 에서 정의된 실제 데이터</td>
      <td style="background:#f8d7da;">x</td>
      <td style="background:#f8d7da;">double</td>
      <td></td>
    </tr>

    <tr>
      <td style="background:#f8d7da;">y</td>
      <td style="background:#f8d7da;">double</td>
      <td></td>
    </tr>

    <tr>
      <td style="background:#f8d7da;">z</td>
      <td style="background:#f8d7da;">double</td>
      <td></td>
    </tr>

    <tr>
      <td style="background:#f8d7da;">intensity</td>
      <td style="background:#f8d7da;">unsigned char</td>
      <td></td>
    </tr>

    <tr>
      <td style="background:#f8d7da;">laser_id</td>
      <td style="background:#f8d7da;">unsigned char</td>
      <td></td>
    </tr>

    <tr>
      <td>is_dense</td>
      <td>bool</td>
      <td>유효하지 않은 점의 유무</td>
      <td></td>
      <td></td>
      <td>false로 지정</td>
    </tr>
  </tbody>
</table>
