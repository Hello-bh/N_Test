<style>
  table.pc2-table {
    width: 100%;
    border-collapse: collapse;
    table-layout: fixed;
    font-size: 14px;
  }

  .pc2-table th,
  .pc2-table td {
    border: 1px solid #444;
    padding: 8px;
    vertical-align: middle;
  }

  .pc2-table th {
    text-align: center;
    font-weight: bold;
    background: #f5f5f5;
  }

  .pc2-table td.text {
    text-align: left;
    word-break: break-word;
  }

  .highlight {
    background-color: #f8d7da;
  }

  /* 열 너비 조절 */
  .col-field { width: 10%; }
  .col-type  { width: 12%; }
  .col-desc  { width: 28%; }
</style>

<table class="pc2-table">
  <thead>
    <tr>
      <th colspan="3">ROS (PointCloud2)</th>
      <th colspan="3">SDR (range)</th>
    </tr>
    <tr>
      <th class="col-field">필드</th>
      <th class="col-type">데이터 타입</th>
      <th class="col-desc">설명</th>
      <th class="col-field">필드</th>
      <th class="col-type">데이터 타입</th>
      <th class="col-desc">설명 (XROS2 사용)</th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>header</td>
      <td></td>
      <td class="text">time(sec, nsec) + frame_id</td>
      <td class="highlight">time</td>
      <td class="highlight">string</td>
      <td class="text highlight">sec + . + nsec 로 변환</td>
    </tr>

    <tr>
      <td>height</td>
      <td>uint32</td>
      <td class="text">기기 마다 다른 고정값, 1채널</td>
      <td></td>
      <td></td>
      <td class="text">임의로 1 지정</td>
    </tr>

    <tr>
      <td>width</td>
      <td>uint32</td>
      <td class="text">기기 마다 다른 고정값, 채널 개수</td>
      <td></td>
      <td></td>
      <td class="text">1회전에 생산되는 포인트 개수</td>
    </tr>

    <tr>
      <td>fields</td>
      <td></td>
      <td class="text">x, y, z 등의 위치와 데이터 정의</td>
      <td></td>
      <td></td>
      <td class="text"></td>
    </tr>

    <tr>
      <td>point_step</td>
      <td>uint32</td>
      <td class="text">1 point의 byte</td>
      <td></td>
      <td></td>
      <td class="text">1 point의 byte</td>
    </tr>

    <tr>
      <td>row_step</td>
      <td>uint32</td>
      <td class="text">point_step × width</td>
      <td></td>
      <td></td>
      <td class="text">point_step × width</td>
    </tr>

    <tr>
      <td rowspan="5">data</td>
      <td rowspan="5">uint8[]</td>
      <td rowspan="5" class="text">fields 에서 정의된 실제 데이터</td>

      <td class="highlight">x</td>
      <td class="highlight">double</td>
      <td class="text"></td>
    </tr>

    <tr>
      <td class="highlight">y</td>
      <td class="highlight">double</td>
      <td class="text"></td>
    </tr>

    <tr>
      <td class="highlight">z</td>
      <td class="highlight">double</td>
      <td class="text"></td>
    </tr>

    <tr>
      <td class="highlight">intensity</td>
      <td class="highlight">unsigned char</td>
      <td class="text"></td>
    </tr>

    <tr>
      <td class="highlight">laser_id</td>
      <td class="highlight">unsigned char</td>
      <td class="text"></td>
    </tr>

    <tr>
      <td>is_dense</td>
      <td>bool</td>
      <td class="text">유효하지 않은 점의 유무</td>
      <td></td>
      <td></td>
      <td class="text">false로 지정</td>
    </tr>
  </tbody>
</table>
