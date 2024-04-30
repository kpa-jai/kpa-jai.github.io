---
layout: page
title: Kurikulum
permalink: /kpa/kurikulum
---

<ul>
  <li><a href="https://docs.google.com/spreadsheets/d/1XgVwDE2T7K3WsKemb-fK1tDdD0C-1_VtzrYAj3BxtZw/" target="_blank">File Kurikulum KPA Pusat</a></li>
</ul>

Catatan: 

<ul>
  <li>Hanya yang diberikan akses oleh panitia yang bisa untuk mengakses file di atas.</li>
  <li>Mohon menghubungi panitia pusat untuk mendapatkan akses file ini.</li>
</ul>

### Kelas

<table>
  <thead>
    <tr>
      <th>No.</th>
      <th>Kelas</th>
      <th>Rentang Usia</th>
    </tr>
  </thead>
  <tbody>
  {% for db in site.data.db-kelas %}
    <tr>
      <td>{{ db.no }}</td>
      <td>{{ db.kelas }}</td>
      <td>{{ db.rentang-usia }}</td>
    </tr>
  {% endfor %}  
  </tbody>
</table>

### Kurikulum Sepekan

<table>
  <thead>
    <tr>
      <th>No.</th>
      <th>Kelas</th>
      <th>Mata Pelajaran</th>
      <th>Target Pembelajaran</th>
    </tr>
  </thead>
  <tbody>
  {% for db in site.data.db-kurikulum-sepekan %}
    <tr>
      <td>{{ db.no }}</td>
      <td>{{ db.kelas }}</td>
      <td>{{ db.mata-pelajaran }}</td>
      <td>{{ db.target-pembelajaran-sepekan }}</td>
    </tr>
  {% endfor %}  
  </tbody>
</table>

### Kurikulum Harian

<table>
  <thead>
    <tr>
      <th>No.</th>
      <th>Tgl</th>
      <th>Kelas</th>
      <th>Pelajaran</th>
      <th>Target Pembelajaran</th>
    </tr>
  </thead>
  <tbody>
  {% for db in site.data.db-kurikulum %}
    <tr>
      <td>{{ db.no }}</td>
      <td>{{ db.tanggal }}</td>
      <td>{{ db.kelas }}</td>
      <td>{{ db.mata-pelajaran }}</td>
      <td>{{ db.target-pembelajaran }}</td>
    </tr>
  {% endfor %}
  </tbody>
</table>