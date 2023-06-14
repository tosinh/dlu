<script>
    const itemsFunctionalRooms = [
        {
            id: 1,
            label: "Phòng Tổ chức hành chính",
            href: "https://tchc.dlu.edu.vn/",
        },
        {
            id: 2,
            label: "Phòng Quản lý Đào tạo",
            href: "https://pqldt.dlu.edu.vn/",
        },
        {
            id: 3,
            label: "Phòng Chính trị và Công tác Sinh viên",
            href: "https://pctsv.dlu.edu.vn/",
        },
        {
            id: 4,
            label: "Phòng Quản lý Chất lượng",
            href: "https://pktkd.dlu.edu.vn/",
        },
        {
            id: 5,
            label: "Phòng Quản lý Khoa học – Hợp tác Quốc tế",
            href: "https://pkhht.dlu.edu.vn/",
        },
        {
            id: 6,
            label: "Phòng Thanh Tra",
            href: "https://ptt.dlu.edu.vn/",
        },
        {
            id: 7,
            label: "Phòng Tài Chính",
            href: "https://ptc.dlu.edu.vn/",
        },
        {
            id: 8,
            label: "Phòng Cơ sở Vật chất",
            href: "https://pcsvc.dlu.edu.vn/",
        },
        {
            id: 9,
            label: "Phòng Quản lý Đào tạo Sau Đại học",
            href: "https://sdh.dlu.edu.vn/",
        },
        {
            id: 10,
            label: "Phòng Tạp chí và Truyền Thông",
            href: "https://ptctt.dlu.edu.vn/",
        },
    ];
    const itemsDepartments = [
        {
            id: 1,
            label: "Khoa Toán – Tin",
            href: "http://ktt.dlu.edu.vn/",
        },
        {
            id: 2,
            label: "Khoa Công nghệ Thông tin",
            href: "http://cntt.dlu.edu.vn/",
        },
        {
            id: 3,
            label: "Khoa Vật lý và Kỹ thuật hạt nhân",
            href: "http://vl.dlu.edu.vn/",
        },
        {
            id: 4,
            label: "Khoa Hóa học và Môi trường",
            href: "http://khhmt.dlu.edu.vn/",
        },
        {
            id: 5,
            label: "Khoa Sinh học",
            href: "http://ksh.dlu.edu.vn/",
        },
        {
            id: 6,
            label: "Khoa Nông lâm",
            href: "http://knl.dlu.edu.vn/",
        },
        {
            id: 7,
            label: "Khoa Ngữ văn và Lịch sử",
            href: "http://nvvh.dlu.edu.vn/",
        },
        {
            id: 8,
            label: "Khoa Kinh tế – Quản trị Kinh doanh",
            href: "http://kktqt.dlu.edu.vn/",
        },
        {
            id: 9,
            label: "Khoa Du lịch",
            href: "https://kdl.dlu.edu.vn/",
        },
        {
            id: 10,
            label: "Khoa Luật học",
            href: "http://klh.dlu.edu.vn/",
        },
        {
            id: 11,
            label: "Khoa Ngoại ngữ",
            href: "http://nn.dlu.edu.vn/",
        },
        {
            id: 12,
            label: "Khoa Quốc tế học",
            href: "http://kqth.dlu.edu.vn/",
        },
        {
            id: 13,
            label: "Khoa Xã hội học và Công tác xã hội",
            href: "http://kctxh.dlu.edu.vn/",
        },
        {
            id: 14,
            label: "Khoa Sư phạm",
            href: "http://sp.dlu.edu.vn/",
        },
        {
            id: 15,
            label: "Khoa Lý luận Chính trị",
            href: "http://kllct.dlu.edu.vn/",
        },
        {
            id: 16,
            label: "Khoa Giáo dục Quốc phòng – An ninh và Thể chất",
            href: "http://kgdtc.dlu.edu.vn/",
        },
    ];
</script>

<footer>
    <div class="wrap-footer grid grid-cols-3 gap-4">
        <div class="footer-F">
            <h4>CÁC PHÒNG CHỨC NĂNG</h4>
            <ul class="footer-F-list">
                {#each itemsFunctionalRooms as itemF (itemF.id)}
                    <li class="footer-F-item">
                        <svg
                            fill="#ffffff"
                            xmlns="http://www.w3.org/2000/svg"
                            viewBox="0 0 24 24"
                            id="right-arrow"
                            width="16px"
                            height="16px"
                            ><path
                                d="M15.54,11.29,9.88,5.64a1,1,0,0,0-1.42,0,1,1,0,0,0,0,1.41l4.95,5L8.46,17a1,1,0,0,0,0,1.41,1,1,0,0,0,.71.3,1,1,0,0,0,.71-.3l5.66-5.65A1,1,0,0,0,15.54,11.29Z"
                            /></svg
                        >
                        <a href={itemF.href}>{itemF.label}</a>
                    </li>
                {/each}
            </ul>
        </div>
        <div class="footer-D">
            <h4>CÁC KHOA</h4>
            <ul class="footer-D-list">
                {#each itemsDepartments as itemD (itemD.id)}
                    <li class="footer-D-item">
                        <svg
                            fill="#ffffff"
                            xmlns="http://www.w3.org/2000/svg"
                            viewBox="0 0 24 24"
                            id="right-arrow"
                            width="16px"
                            height="16px"
                            ><path
                                d="M15.54,11.29,9.88,5.64a1,1,0,0,0-1.42,0,1,1,0,0,0,0,1.41l4.95,5L8.46,17a1,1,0,0,0,0,1.41,1,1,0,0,0,.71.3,1,1,0,0,0,.71-.3l5.66-5.65A1,1,0,0,0,15.54,11.29Z"
                            /></svg
                        >
                        <a href={itemD.href}>{itemD.label}</a>
                    </li>
                {/each}
            </ul>
        </div>
        <div class="footer-I">
            <h4>TRƯỜNG ĐẠI HỌC ĐÀ LẠT</h4>
            <ul class="footer-I-list">
                <li class="footer-I-item">
                    <svg
                        version="1.1"
                        fill="#ffffff"
                        id="_x32_"
                        xmlns="http://www.w3.org/2000/svg"
                        xmlns:xlink="http://www.w3.org/1999/xlink"
                        width="20px"
                        height="20px"
                        viewBox="0 0 512 512"
                        xml:space="preserve"
                    >
                        <g>
                            <path
                                class="st0"
                                d="M256,0C159.969,0,82.125,77.859,82.125,173.906C82.125,269.938,236.797,512,256,512
            c19.219,0,173.875-242.063,173.875-338.094C429.875,77.859,352.031,0,256,0z M256,240.406c-36.719,0-66.5-29.781-66.5-66.5
            c0-36.75,29.781-66.531,66.5-66.531s66.516,29.781,66.516,66.531C322.516,210.625,292.719,240.406,256,240.406z"
                            />
                        </g>
                    </svg>
                    1 Phù Đổng Thiên Vương - P8 - TP.Đà Lạt
                </li>
                <li class="footer-I-item">
                    <svg
                        fill="#ffffff"
                        width="20px"
                        height="20px"
                        viewBox="0 0 32 32"
                        xmlns="http://www.w3.org/2000/svg"
                        ><path
                            d="M11.748 5.773S11.418 5 10.914 5c-.496 0-.754.229-.926.387S6.938 7.91 6.938 7.91s-.837.731-.773 2.106c.054 1.375.323 3.332 1.719 6.058 1.386 2.72 4.855 6.876 7.047 8.337 0 0 2.031 1.558 3.921 2.191.549.173 1.647.398 1.903.398.26 0 .719 0 1.246-.385.536-.389 3.543-2.807 3.543-2.807s.736-.665-.119-1.438c-.859-.773-3.467-2.492-4.025-2.944-.559-.459-1.355-.257-1.699.054-.343.313-.956.828-1.031.893-.112.086-.419.365-.763.226-.438-.173-2.234-1.148-3.899-3.426-1.655-2.276-1.837-3.02-2.084-3.824a.56.56 0 0 1 .225-.657c.248-.172 1.161-.933 1.161-.933s.591-.583.344-1.27-1.906-4.716-1.906-4.716z"
                        /></svg
                    >
                    <a href="tel:0263 3822 246">0263 3822 246</a>
                    0263 3822 246 | Fax:
                    <a href="teL:0263.3823380">0263.3823380</a>
                </li>
                <li class="footer-I-item">
                    <svg
                        fill="#ffffff"
                        width="20px"
                        height="20px"
                        viewBox="0 0 32 32"
                        xmlns="http://www.w3.org/2000/svg"
                        ><path
                            d="M5 24.225V7.776h22v16.447H5v.002zm3.011-1.815h15.978l-5.111-5.115L16 20.179l-2.877-2.883-5.112 5.114zm-1.216-1.275l5.077-5.09-5.077-5.065v10.155zm13.332-5.09l5.079 5.09V10.979l-5.079 5.066zm-4.126 1.588l8.022-8.027-16.045-.001 8.023 8.028z"
                        /></svg
                    >
                    <a href="mailto:info@dlu.edu.vn">daihocdalat@dlu.edu.vn</a>
                </li>
            </ul>
        </div>
    </div>
    <div class="footer-buttom">
        <span
            >Copyright © 2020 Trung tâm Công nghệ Thông tin Trường Đại học Đà
            Lạt</span
        >
    </div>
</footer>

<style>
    footer {
        background-color: #5f7adb;
        margin-top: 100px;
    }
    .wrap-footer {
        width: 1200px;
        max-width: 100%;
        margin: 0 auto;
        padding: 40px 0 0;
    }
    h4 {
        color: white;
        font-size: 24px;
        font-weight: 600;
        margin: 10px;
    }
    li {
        color: #fff;
        margin-top: 5px;
    }
    .footer-F-item,
    .footer-D-item {
        display: flex;
    }
    .footer-I-item {
        display: flex;
    }
    svg {
        margin: 3px 4px 0;
    }
    .footer-buttom {
        margin-top: 20px;
        background-color: #514939;
    }
    .footer-buttom span {
        color: #fff;
        font-size: 12px;
        line-height: 40px;
        margin-left: 10%;
    }
</style>
