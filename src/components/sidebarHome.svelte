<script>
    import { page } from "$app/stores";
    import {
        Sidebar,
        SidebarGroup,
        SidebarItem,
        SidebarWrapper,
        SidebarDropdownWrapper,
        SidebarDropdownItem,
    } from "flowbite-svelte";
    let spanClass = "flex-1 ml-3 whitespace-nowrap";
    $: activeUrl = $page.url.pathname;
    $: containPath = () => {
        // add your logic here
        true;
    };
</script>

<Sidebar>
    <SidebarWrapper>
        <SidebarGroup>
            <SidebarItem label="Trang Chủ" />
            <SidebarDropdownWrapper label="Giới thiệu">
                <SidebarDropdownItem
                    label="Giá trị cốt lõi, định hướng, sứ mạng, mục tiêu"
                    href=""
                />
                <SidebarDropdownItem
                    label="Lịch sử hình thành và phát triển"
                    href=""
                />
                <SidebarDropdownWrapper label="Cơ cấu tổ chức">
                    <SidebarDropdownItem label="Đảng Uỷ" href="" />
                    <SidebarDropdownItem label="Hội đồng trường" href="" />
                    <SidebarDropdownItem label="Ban Giám hiệu" href="" />
                </SidebarDropdownWrapper>
            </SidebarDropdownWrapper>
            <SidebarDropdownWrapper label="Đào tạo">
                <SidebarDropdownItem label="Tiến sĩ" href="" />
                <SidebarDropdownItem label="Thạc sĩ" href="" />
                <SidebarDropdownItem label="Đại học chính quy" href="" />
                <SidebarDropdownItem label="Đại học vừa làm vừa học" href="" />
                <SidebarDropdownItem label="Đề án mở ngành" href="" />
                <SidebarDropdownItem label="Chương trình đào tạo" href="" />
            </SidebarDropdownWrapper>
            <SidebarDropdownWrapper label="Khoa">
                <SidebarDropdownItem label="Khoa Toán – Tin" href="" />
                <SidebarDropdownItem label="Khoa Công nghệ Thông tin" href="" />
                <SidebarDropdownItem
                    label="Khoa Vật lý và Kỹ thuật hạt nhân"
                    href=""
                />
                <SidebarDropdownItem
                    label="Khoa Hóa học và Môi trường"
                    href=""
                />
                <SidebarDropdownItem label="Khoa Sinh học" href="" />
                <SidebarDropdownItem label="Khoa Nông lâm" href="" />
                <SidebarDropdownItem label="Khoa Ngữ văn và Lịch sử" href="" />
                <SidebarDropdownItem
                    label="Khoa Kinh tế – Quản trị Kinh doanh"
                    href=""
                />
                <SidebarDropdownItem label="Khoa Du lịch" href="" />
                <SidebarDropdownItem label="Khoa Luật học" href="" />
                <SidebarDropdownItem label="Khoa Ngoại ngữ" href="" />
                <SidebarDropdownItem label="Khoa Quốc tế học" href="" />
                <SidebarDropdownItem
                    label="Khoa Xã hội học và Công tác xã hội"
                    href=""
                />
                <SidebarDropdownItem label="Khoa Sư phạm" href="" />
                <SidebarDropdownItem label="Khoa Lý luận Chính trị" href="" />
                <SidebarDropdownItem
                    label="Khoa Giáo dục Quốc phòng – An ninh và Thể chất"
                    href=""
                />
            </SidebarDropdownWrapper>
            <SidebarDropdownWrapper label="Phòng">
                <SidebarDropdownItem label="Phòng Tổ chức hành chính" href="" />
                <SidebarDropdownItem label="Phòng Quản lý Đào tạo" href="" />
                <SidebarDropdownItem
                    label="Phòng Chính trị và Công tác Sinh viên"
                    href=""
                />
                <SidebarDropdownItem label="Phòng Quản lý Chất lượng" href="" />
                <SidebarDropdownItem
                    label="Phòng Quản lý Khoa học – Hợp tác Quốc tế"
                    href=""
                />
                <SidebarDropdownItem label="Phòng Thanh Tra" href="" />
                <SidebarDropdownItem label="Phòng Tài Chính" href="" />
                <SidebarDropdownItem label="Phòng Cơ sở Vật chất" href="" />
                <SidebarDropdownItem
                    label="Phòng Quản lý Đào tạo Sau Đại học"
                    href=""
                />
                <SidebarDropdownItem
                    label="Phòng Tạp chí và Truyền Thông"
                    href=""
                />
            </SidebarDropdownWrapper>
            <SidebarDropdownWrapper label="Viện">
                <SidebarDropdownItem
                    label="Viện Nghiên cứu và Ứng dụng Nông nghiệp Công nghệ cao"
                    href=""
                />
            </SidebarDropdownWrapper>
            <SidebarDropdownWrapper label="Trung Tâm">
                <SidebarDropdownItem
                    label="Trung tâm Công nghệ thông tin"
                    href=""
                />
                <SidebarDropdownItem
                    label="Trung tâm Ngoại ngữ và Đào tạo nguồn nhân lực"
                    href=""
                />
                <SidebarDropdownItem
                    label="Trung tâm Hỗ trợ Khởi nghiệp"
                    href=""
                />
                <SidebarDropdownItem
                    label="Trung tâm Phân tích và Kiểm định"
                    href=""
                />
                <SidebarDropdownItem
                    label="Trung tâm Giáo dục Đào tạo Trí tuệ Nhân tạo"
                    href=""
                />
                <SidebarDropdownItem label="" href="" />
            </SidebarDropdownWrapper>
            <SidebarItem label="Thư Viện" />
            <SidebarItem label="QLGD" />
            <SidebarDropdownWrapper label="Đảng – Đoàn Thể">
                <SidebarDropdownItem label="Đảng bộ" href="" />
                <SidebarDropdownItem label="Công đoàn" href="" />
                <SidebarDropdownItem label="Đoàn Thanh Niên" href="" />
                <SidebarDropdownItem label="Hội Sinh viên" href="" />
                <SidebarDropdownItem label="Hội Cựu Chiến Binh" href="" />
            </SidebarDropdownWrapper>
            <SidebarItem label="Cán bộ/Giảng viên" />
            <SidebarItem label="Sinh Viên" />
            <SidebarItem label="Liên Hệ" />
        </SidebarGroup>
    </SidebarWrapper>
</Sidebar>
