<script setup>
import { Navbar, NavbarLogo, NavbarCollapse, NavbarLink } from 'flowbite-vue'
import { Carousel } from 'flowbite-vue'
import { Table, TableHead, TableBody, TableHeadCell, TableRow, TableCell } from 'flowbite-vue'
import { Progress } from 'flowbite-vue'
import { Timeline, TimelineItem, TimelinePoint, TimelineContent, TimelineTitle } from 'flowbite-vue'
import { Input } from 'flowbite-vue'
import { Pagination } from 'flowbite-vue'
import { ref } from 'vue'

const currentPage = ref(1)
import { Footer } from 'flowbite-vue'
const pictures = [
  {
    'src': 'https://flowbite.s3.amazonaws.com/docs/gallery/featured/image.jpg',
    'alt': 'Picture 1',
  },
  {
    'src': 'https://glamlelaki.my/wp-content/uploads/2021/04/APPLE-SPRING-LOADED-EVENT-3-PRODUK-TERBARU.jpg',
    'alt': 'Picture 2',
  },
  {
    'src': 'https://www.intego.com/mac-security-blog/wp-content/uploads/2021/05/imac-ipad-600.jpg',
    'alt': 'Picture 3',
  },
];
</script>
<style>
table{
  margin: 20px;
}

Pagination{
  margin: 20px;
  display: flex;
}

placeholder{
  margin: 20px;

}
label{
  margin: 20px;
}
Timeline{
  margin: 20px;
}
    .my-6{
      margin:20px;
    }
    .my-6 h6{
      margin:20px 0;
    }
  </style>
<template>
    <Navbar solid>
      <template #logo>
        <NavbarLogo link="https://www.google.com/" alt="Flowbite logo" image-url="https://flowbite.com/docs/images/logo.svg">
          Data Apple
        </NavbarLogo>
      </template>
      <template #default="{isShowMenu}">
        <NavbarCollapse :isShowMenu="isShowMenu">
          <NavbarLink is-active>Home</NavbarLink>
          <NavbarLink a href>Product</NavbarLink>
          <NavbarLink a href>Penjualan</NavbarLink>
        </NavbarCollapse>
      </template>
    </Navbar>

    <Carousel :pictures="pictures"></Carousel>

    <Table hoverable class="my-12">
    <table-head>
      <table-head-cell>Product name</table-head-cell>
      <table-head-cell>Color</table-head-cell>
      <table-head-cell>Category</table-head-cell>
      <table-head-cell>Price</table-head-cell>
      <table-head-cell><span class="sr-only">Edit</span></table-head-cell>
    </table-head>
    <table-body>
      <table-row>
        <table-cell>Apple MacBook Pro 17"</table-cell>
        <table-cell>Sliver</table-cell>
        <table-cell>Laptop</table-cell>
        <table-cell>Rp 19.999.000</table-cell>
        <table-cell>
          <a href="#" class="font-medium text-blue-600 dark:text-blue-500 hover:underline">Edit</a>
        </table-cell>
      </table-row>
      <table-row>
        <table-cell>Microsoft Surface Pro</table-cell>
        <table-cell>White</table-cell>
        <table-cell>Laptop PC</table-cell>
        <table-cell>Rp 17.599.000</table-cell>
        <table-cell>
          <a href="#" class="font-medium text-blue-600 dark:text-blue-500 hover:underline">Edit</a>
        </table-cell>
      </table-row>
      <table-row>
        <table-cell>Magic Mouse 2</table-cell>
        <table-cell>Black</table-cell>
        <table-cell>Accessories</table-cell>
        <table-cell>Rp 2.100.000</table-cell>
        <table-cell>
          <a href="#" class="font-medium text-blue-600 dark:text-blue-500 hover:underline">Edit</a>
        </table-cell>
      </table-row>
      <table-row>
        <table-cell>Smart Watch</table-cell>
        <table-cell>Black</table-cell>
        <table-cell>Accessories</table-cell>
        <table-cell>Rp 5.800.000</table-cell>
        <table-cell>
          <a href="#" class="font-medium text-blue-600 dark:text-blue-500 hover:underline">Edit</a>
        </table-cell>
      </table-row>
      <table-row>
        <table-cell>Smart Watch</table-cell>
        <table-cell>Gray</table-cell>
        <table-cell>Accessories</table-cell>
        <table-cell>Rp 5.100.000</table-cell>
        <table-cell>
          <a href="#" class="font-medium text-blue-600 dark:text-blue-500 hover:underline">Edit</a>
        </table-cell>
      </table-row>
      <table-row>
        <table-cell>Ipad Max</table-cell>
        <table-cell>Green</table-cell>
        <table-cell>Accessories</table-cell>
        <table-cell>Rp 8.990.000</table-cell>
        <table-cell>
          <a href="#" class="font-medium text-blue-600 dark:text-blue-500 hover:underline">Edit</a>
        </table-cell>
      </table-row>
      <table-row>
        <table-cell>Ipad Pro Max</table-cell>
        <table-cell>Black</table-cell>
        <table-cell>Accessories</table-cell>
        <table-cell>Rp 9.100.000</table-cell>
        <table-cell>
          <a href="#" class="font-medium text-blue-600 dark:text-blue-500 hover:underline">Edit</a>
        </table-cell>
      </table-row>
    </table-body>
  </Table>

  <div class="my-6">
    <h6 >Penjualan Apple MacBook Pro 17</h6>
  <Progress labelProgress="true" labelPosition="inside" size="lg" progress="61"></Progress>
  <h6>Penjualan Microsoft Surface Pro</h6>
  <Progress labelProgress="true" labelPosition="inside" size="lg" progress="25"></Progress>
  <h6>Penjualan Magic Mouse 2</h6>
  <Progress labelProgress="true" labelPosition="inside" size="lg" progress="75"></Progress>
  <h6>Penjualan Smart Wacth </h6>
  <Progress labelProgress="true" labelPosition="inside" size="lg" progress="65"></Progress>
  <h6>Penjualan Smart Wacth</h6>
  <Progress labelProgress="true" labelPosition="inside" size="lg" progress="75"></Progress>
  <h6>Penjualan Ipad Max</h6>
  <Progress labelProgress="true" labelPosition="inside" size="lg" progress="45"></Progress>
  <h6>Penjualan Ipad Pro Max</h6>
  <Progress labelProgress="true" labelPosition="inside" size="lg" progress="55"></Progress>
  </div>

  <Timeline class="my-12">
    <timeline-item>
      <timeline-point>
        <svg aria-hidden="true" class="w-3 h-3 text-blue-600 dark:text-blue-400" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg"><path fill-rule="evenodd" d="M6 2a1 1 0 00-1 1v1H4a2 2 0 00-2 2v10a2 2 0 002 2h12a2 2 0 002-2V6a2 2 0 00-2-2h-1V3a1 1 0 10-2 0v1H7V3a1 1 0 00-1-1zm0 5a1 1 0 000 2h8a1 1 0 100-2H6z" clip-rule="evenodd"></path></svg>
      </timeline-point>
      <timeline-content>
        <timeline-title>
              Juni 2014
        </timeline-title>
        <timeline-body>
          Produk pertama mulai di munculkan dengan harapan terjual sesuai target 10.000 unit dalam kurung waktu 1 tahun.
        </timeline-body>
      </timeline-content>
    </timeline-item>
    <timeline-item>
      <timeline-point>
        <svg aria-hidden="true" class="w-3 h-3 text-blue-600 dark:text-blue-400" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg"><path fill-rule="evenodd" d="M6 2a1 1 0 00-1 1v1H4a2 2 0 00-2 2v10a2 2 0 002 2h12a2 2 0 002-2V6a2 2 0 00-2-2h-1V3a1 1 0 10-2 0v1H7V3a1 1 0 00-1-1zm0 5a1 1 0 000 2h8a1 1 0 100-2H6z" clip-rule="evenodd"></path></svg>
      </timeline-point>
      <timeline-content>
        <timeline-title>
              September 2918
        </timeline-title>
        <timeline-body>
          Seri Apple watch mulai di luncurkan, dengan target penjualan 3.000 unit dalam kurung waktu 3 bulan.
        </timeline-body>
      </timeline-content>
    </timeline-item>
    <timeline-item>
      <timeline-point>
        <svg aria-hidden="true" class="w-3 h-3 text-blue-600 dark:text-blue-400" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg"><path fill-rule="evenodd" d="M6 2a1 1 0 00-1 1v1H4a2 2 0 00-2 2v10a2 2 0 002 2h12a2 2 0 002-2V6a2 2 0 00-2-2h-1V3a1 1 0 10-2 0v1H7V3a1 1 0 00-1-1zm0 5a1 1 0 000 2h8a1 1 0 100-2H6z" clip-rule="evenodd"></path></svg>
      </timeline-point>
      <timeline-content>
        <timeline-title>
              juli 2022
        </timeline-title>
        <timeline-body>
          Seri terbaru MacBook mulai di buat dengan target penyelesaian 100 unit per minggunya.
        </timeline-body>
      </timeline-content>
    </timeline-item>
  </Timeline>

  <Input size="sm" placeholder="enter your first name" label="First name">
    <template #helper>
    </template>
  </Input>

  <Input size="sm" placeholder="enter your email" label="Email">
    <template #helper>
    </template>
  </Input>

  <Input size="md" placeholder="enter your comment" label="Comment">
    <template #helper>
    </template>
  </Input>

  <Pagination v-model="currentPage" :total-pages="100" show-icons></Pagination>

  <Footer style="background-color: skyblue; "></Footer>
</template>
