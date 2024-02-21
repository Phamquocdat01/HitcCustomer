<!-- <template>
  <q-page>
<div class=" items-center shadow-1 example-column-all-breakpoints no-wrap">
  <div class="col-2">
    <div class="row items-center shadow-1" style="height: 70px" >
              <div  class=" q-ml-md q-gutter-md text-subtitle1 row items-center">
                <a href="#">DANH SÁCH VẤN ĐỀ CỦA CS </a>
                <a href="#">DANH SÁCH HAPPY CALL</a>
              </div>
              <q-space/>
              <q-btn class="q-mr-md" color="indigo-14" label="Thêm" />
              <q-btn class="q-mr-md" color="indigo-14" label="Xuất Excel" />
            </div>
            </div>
  <div class="col-2">
    <div class="row items-center shadow-1 example-row-all-breakpoints" style="height: 70px">
    <q-item-label class=" q-mx-md">Lọc dữ liệu</q-item-label>
            <div class=" row q-px-xs ">
            <div class="row items-center q-gutter-xs ">
              <q-select
                filled
                v-model="model"
                clearable
                use-input
                hide-selected
                fill-input
                input-debounce="0"
                label="Nhập từ khóa"
                :options="options"
                @filter="filterFn"
                @filter-abort="abortFilterFn"
                style="width: 600px"
              >
                <template v-slot:no-option>
                  <q-item>
                    <q-item-section class="text-grey">
                      No results
                    </q-item-section>
                  </q-item>
                </template>
              </q-select>
          </div>
        </div>
        <q-btn class="q-mx-xs" color="indigo-14" icon="search" label="Lấy dữ liệu" />
        <q-space/>
        <q-btn class="q-mr-md" color="indigo-14" icon="tune" />
    </div>
    </div>
    <div class=" items-center shadow-1 example-column-all-breakpoints no-wrap">
    <div class="col-6 ">
    <q-option-group
      v-model="separator"
      inline
      class="q-ma-md"
      :options="[
        { label: 'Horizontal (default)', value: 'horizontal' },
        { label: 'Vertical', value: 'vertical' },
        { label: 'Cell', value: 'cell' },
        { label: 'None', value: 'none' },
      ]"
    />
     <q-table
      flat bordered
      :rows="rows"
      :columns="columns"
      row-key="name"
      :separator="separator"
    />
  </div>
    </div>
  </div>
</q-page>
</template>

<script>
import { defineComponent, ref } from 'vue'
const columns = [
  {
    name: 'name',
    required: true,
    label: 'Loại vấn đề',
    align: 'left',
    field: row => row.name,
    format: val => `${val}`,
    sortable: true
  },
  { name: 'SĐT', align: 'center', label: 'SĐT', field: 'SĐT', sortable: true },
  { name: 'TKH', label: 'Tên khách hàng', field: 'TKH', sortable: true },
  { name: 'ĐC', label: 'Địa chỉ', field: 'ĐC' },
  { name: 'ND', label: 'Nội dung', field: 'ND' },
  { name: 'TL', label: 'Trả lời', field: 'TL' },
  { name: 'NT', label: 'Người tạo', field: 'NT' },
  { name: 'NgT', label: 'Ngày tạo', field: 'NgT' },
  { name: 'TT', label: 'Trạng thái', field: 'TT' },
  { name: 'NHT', label: 'Ngày hoàn thành', field: 'NHT' },
  { name: 'CN', label: 'Chức năng', field: 'CN' }
]

const rows = [
  {
    name: 'Hỗ trợ thanh toán tra cước',
    SĐT: 159,
    TKH: 11223344,
    ĐC: 24,
    ND: 'Khách hàng hỏi về cước',
    TL: 'Đã phản hồi khách hàng',
    NT: 'HTC',
    NgT: '12/07/2023',
    TT: 'Open',
    NHT: '17/07/2023',
    CN: 3
  },
  {
    name: 'Khiếu nại',
    SĐT: 159,
    TKH: 6.0,
    ĐC: 24,
    ND: 4.0,
    TL: 87,
    NT: '14%',
    NgT: '1%',
    TT: 1,
    NHT: 2,
    CN: 3
  },
  {
    name: 'Sự cố',
    SĐT: 159,
    TKH: 6.0,
    ĐC: 24,
    ND: 4.0,
    TL: 87,
    NT: '14%',
    NgT: '1%',
    TT: 1,
    NHT: 2,
    CN: 3
  },
  {
    name: 'Tra cứu thông tin',
    SĐT: 159,
    TKH: 6.0,
    ĐC: 24,
    ND: 4.0,
    TL: 87,
    NT: '14%',
    NgT: '1%',
    TT: 1,
    NHT: 2,
    CN: 3
  },
  {
    name: 'Tư vấn dịch vụ',
    SĐT: 159,
    TKH: 6.0,
    ĐC: 24,
    ND: 4.0,
    TL: 87,
    NT: '14%',
    NgT: '1%',
    TT: 1,
    NHT: 2,
    CN: 3
  },
  {
    name: 'Yêu cầu thanh lý',
    SĐT: 159,
    TKH: 6.0,
    ĐC: 24,
    ND: 4.0,
    TL: 87,
    NT: '14%',
    NgT: '1%',
    TT: 1,
    NHT: 2,
    CN: 3
  }
]

export default defineComponent({
  name: 'IndexPage',
  setup () {
    return {
      separator: ref('vertical'),
      columns,
      rows
    }
  }
})
</script>
<style scoped>

a{
  color: #304FFe;
  text-decoration: none;
}
a:hover {
    opacity: 0.7;
}

.row .col-3{
  width: 15%;
}

</style> -->

<template>
  <div class="q-pa-md q-gutter-sm">
    <div class="row items-center shadow-1" style="height: 70px">
      <div class="q-ml-md q-gutter-md text-subtitle1 row items-center">
        <a href="#" class="desline">DANH SÁCH VẤN ĐỀ CỦA CS</a>
        <a href="#">DANH SÁCH HAPPY CALL</a>
      </div>
      <q-space />
      <q-btn
        class="q-mr-md"
        color="primary"
        label="Thêm"
        @click="$router.replace({ name: 'detail' })"
      />
      <q-btn class="q-mr-md" color="primary" label="Xuất Excel" />
    </div>
    <!-- <q-btn
      color="primary"
      label="Thêm"
      @click="$router.replace({ name: 'detail' })"
    />
    <q-btn color="primary" label="Xuất Excel" /> -->
    <q-table
      flat
      bordered
      :rows="data"
      :columns="columns"
      :loading="loading"
      :filter="filter"
      row-key="name"
      @request="fetchData"
    >
      <template v-slot:body="props">
        <q-tr :props="props">
          <q-td key="tenLoaiVanDe" :props="props">{{
            props.row.tenLoaiVanDe
          }}</q-td>
          <q-td key="soDienThoai" :props="props">{{
            props.row.soDienThoai
          }}</q-td>
          <q-td
            key="tenKhachHang"
            :props="props"
            @click="
              $router.push({
                name: 'detailedit',
                params: { id: props.row.id },
              })
            "
          >
            {{ props.row.tenKhachHang }}
          </q-td>
          <q-td key="diaChi" :props="props">{{ props.row.diaChi }}</q-td>
          <q-td key="noiDung" :props="props">{{ props.row.noiDung }}</q-td>
          <q-td key="traLoi" :props="props">{{ props.row.traLoi }}</q-td>
          <q-td key="nguoiTao" :props="props">{{ props.row.nguoiTao }}</q-td>
          <q-td key="ngayTao" :props="props">{{ props.row.ngayTao }}</q-td>
          <q-td key="ngayHoanThanh" :props="props">{{
            props.row.ngayHoanThanh
          }}</q-td>
          <q-td key="ChucNang" :props="props">
            <q-btn
              round
              color="negative"
              size="sm"
              icon="delete"
              @click="confirm(props.row.id)"
            />
          </q-td>
        </q-tr>
      </template>
      <template v-slot:top-left>
        <q-item-label class="q-mx-md items-center">Lọc dữ liệu</q-item-label>
        <q-input
          borderless
          dense
          debounce="300"
          v-model="filter"
          placeholder="Search"
        >
          <template v-slot:append>
            <q-icon name="search" />
          </template>
        </q-input>
      </template>
      <template v-slot:top-right>
        <q-btn class="q-mr-md" color="primary" icon="tune" />
      </template>
    </q-table>
  </div>
</template>

<script>
import { defineComponent, ref } from "vue";
import api from "../app";
import { useQuasar } from "quasar";
// import { data } from 'autoprefixer';
export default defineComponent({
  name: "IndexPage",
  setup() {
    const $q = useQuasar();
    // var pagination = ref({
    //   descending: false,
    //   page: 1,
    //   rowsPerPage: 3,
    //   rowsNumber: 0
    // })
    function confirm(idx) {
      $q.dialog({
        title: "Xác nhận",
        message: "Bạn chắn chắn muốn xóa dữ liệu?",
        cancel: true,
        persistent: true,
      })
        .onOk(() => {
          this.data = api
            .delete(idx)
            .catch((error) =>
              this.$q.notify({
                type: "negative",
                message: "Xóa dữ liệu thất  bại",
              })
            )
            .finally(() =>
              this.$q.notify({
                type: "positive",
                message: "Xóa dữ liệu thành công",
              })
            );
          // console.log('>>>> OK')
        })
        .onOk(() => {
          // console.log('>>>> second OK catcher')
        })
        .onCancel(() => {
          // console.log('>>>> Cancel')
        })
        .onDismiss(() => {
          // console.log('I am triggered on both OK and Cancel')
        });
    }

    return {
      // [
      //   {
      //     tinhTrangModel: null,
      //     uuTienModel: null,
      //     starModel: null,
      //     vanDeModel: null,
      //     sdtModel: null,
      //     tenKhachHangModel: null,
      //     diaChiModel: null,
      //     noiDungModel: null,
      //     traLoiModel: null,
      //     yKienModel: null,
      //     nguoiXulyModel: null,
      //     nguoiTaoModel: null,
      //     ngayTaoModel: null,
      //     ngayHoanThanhModel: null
      //   }
      // ],
      rows: [],
      filter: ref(""),
      confirm,
      // pagination,
      // pagination: ref({
      //   descending: false,
      //   page: 1,
      //   rowsPerPage: 3,
      //   rowsNumber: 0
      // }),
      columns: [
        {
          name: "tenLoaiVanDe",
          label: "Loại vấn đề",
          align: "left",
          field: "tenLoaiVanDe",
          // field: (row) => row.name,
          // format: (val) => `${val}`,
          // sortable: true,
        },
        {
          name: "soDienThoai",
          align: "center",
          label: "SĐT",
          field: "soDienThoai",
        },
        {
          name: "tenKhachHang",
          label: "Tên Khách Hàng",
          field: "tenKhachHang",
        },
        { name: "diaChi", label: "Địa chỉ", field: "diaChi" },
        { name: "noiDung", label: "Nội dung", field: "noiDung" },
        { name: "traLoi", label: "Trả lời", field: "traLoi" },
        { name: "nguoiTao", label: "Người tạo", field: "nguoiTao" },
        { name: "ngayTao", label: "Ngày Tạo", field: "ngayTao" },
        {
          name: "ngayHoanThanh",
          label: "Ngày Hoàn Thành",
          field: "ngayHoanThanh",
        },
        { name: "ChucNang", label: "Chức Năng", field: "ChucNang" },
      ],
    };
  },
  data() {
    return {
      pagination: {
        descending: false,
        page: 1,
        rowsPerPage: 20,
        rowsNumber: 0,
      },
      // pagination: {
      //   page: 1,
      //   rowsPerPage: 3,
      //   rowsNumber: 0
      // },
      loading: false,
      data: [],
    };
  },
  async created() {
    this.fetchData();
  },
  methods: {
    async fetchData() {
      // we can specify the "page" to jump to
      // loading.value = true
      // var check;
      api.getTotal().then((result) => {
        this.pagination.rowsNumber = result;
      });
      // console.log(check)
      // this.pagination.value.rowsNumber = check
      api
        .getAllData(this.pagination.page, this.pagination.rowsPerPage)
        .then((result) => {
          this.data = result.data;
        })
        .catch((error) =>
          this.$q.notify({
            type: "negative",
            message: "Lấy dữ liệu thất  bại",
          })
        )
        .finally(() =>
          this.$q.notify({
            type: "positive",
            message: "Lấy dữ liệu thành công",
          })
        );
      console.log(this.data);
    },
    mounted() {
      this.fetchData({
        pagination: this.pagination,
      });
    },
    // async totalData () {

    // },
    // async fetchData () {
    //   let response
    //   // if (this.isOverview) {
    //     this.data = await api.getAllData().catch((error) => this.$q.notify({
    //                 type: 'negative',
    //                 message: 'Lấy dữ liệu thất  bại'
    //             }))
    //             .finally(() => this.$q.notify({
    //                 type: 'positive',
    //                 message: 'Lấy dữ liệu thành công'
    //             }));
    //   //}
    //   //if (response.Status === 200) {
    //     // this.data = response.data.map(d => {
    //     //   return {
    //     //     LoaiVanDe: d.idLoaiVanDe,
    //     //     TenKhachHang: d.tenKhachHang,
    //     //     PhoneNumber: d.soDienThoai
    //     //   }
    //     // })
    //   //}
    // }
  },
});
</script>


<style scoped>
.desline {
  text-decoration: underline;
}
</style>