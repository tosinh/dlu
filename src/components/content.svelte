<script>
    import { each } from "svelte/internal";

    const newsItems = [
        {
            id: "anh1",
            img: "../src/public/news/anh1.jpg",
            title: "Tuyển sinh đại học 2023 – Những giấy tờ cần chuẩn bị",
            date: "2023-05-15",
            view: "125",
            paragraph:
                "Đợt nhận hồ sơ sớm xét tuyển đại học (hệ chính quy) của Trường Đại học Đà Lạt năm 2023 sắp bắt đầu!!!! (Thời gian chính thức sẽ được cập nhật trong bài viết tiếp theo)",
        },
        {
            id: "anh2",
            img: "../src/public/news/anh2.jpg",
            title: "Khoa học và công nghệ phục vụ phát triển nông nghiệp công nghệ cao tại Lâm Đồng",
            date: "2023-05-13",
            view: "21",
            paragraph:
                " Đây là chủ đề Hội nghị khoa học do Trường Đại học Đà Lạt và Sở Khoa học và Công nghệ tỉnh Lâm Đồng phối hợp tổ chức chiều 12/5 tại Đà Lạt. Hội nghị thu hút 34 đề tài nghiên cứu và tham dự có Phó Chủ tịch UBND tỉnh Lâm Đồng, TS. Phạm S; các GS, PGS, TS, NCS, ThS các trường đại học, Viện nghiên cứu; các chủ doanh nghiệp, nhà quản lý sở, ngành, UBND huyện, thành phố trên địa bàn tỉnh Lâm Đồng…",
        },
        {
            id: "anh3",
            img: "../src/public/news/anh3.png",
            title: "Danh sách đề cử ứng viên tham gia HĐGSCS Trường ĐHĐL năm 2023",
            date: "2023-04-28",
            view: "35",
            paragraph:
                "Thông báo đề cử ứng viên tham gia HĐGSCS Trường Đại học Đà Lạt năm 2023.",
        },
        {
            id: "anh4",
            img: "../src/public/news/anh4.jpg",
            title: "Trường Đại học Đà Lạt xếp hạng thứ 38 trong Top 100 trường đại học tốt nhất Việt Nam",
            date: "2023-03-13",
            view: "130",
            paragraph:
                "Theo kết quả xếp hạng các trường đại học Việt Nam (Viet Nam’s University Rankings – VNUR) năm 2023, Trường Đại học Đà Lạt được xếp thứ 38 trong Top 100 trường đại học tốt nhất ở Việt Nam hiện nay, và là trường có thứ hạng cao nhất ở vùng Tây Nguyên.",
        },
        {
            id: "anh5",
            img: "../src/public/news/anh5.jpg",
            title: "Thông báo v/v mời ứng viên trúng tuyển vòng 1 tham gia phỏng vấn xét tuyển vòng 2, kỳ tuyển dụng viên chức năm 2023 (đợt 1)",
            date: "2023-05-04",
            view: "28",
            paragraph: "",
        },
        {
            id: "anh6",
            img: "../src/public/news/anh6.jpg",
            title: "Thông báo kết quả vòng 1 xét tuyển viên chức năm 2023 (đợt 1)",
            date: "2023-04-27",
            view: "36",
            paragraph: "",
        },
        {
            id: "anh7",
            img: "../src/public/news/anh7.jpg",
            title: "Thông tin các ngành đào tạo và phương thức xét tuyển năm 2023 của Trường Đại học Đà Lạt",
            date: "2023-02-23",
            view: "189",
            paragraph:
                "Thông tin các ngành đào tạo và phương thức xét tuyển năm 2023 của Trường Đại học Đà Lạt",
        },
        {
            id: "anh8",
            img: "../src/public/news/anh8.jpg",
            title: "Trường Đại học Đà Lạt đạt nhiều thành tích tại Hội thao và Hội thi văn nghệ Khối thi đua các trường chuyên nghiệp – cao đẳng – đại học tỉnh Lâm Đồng năm 2023",
            date: "2023-04-29",
            view: "39",
            paragraph:
                "Trường Đại học Đà Lạt đạt nhiều thành tích tại Hội thao và Hội thi văn nghệ Khối thi đua các trường chuyên nghiệp – cao đẳng – đại học tỉnh Lâm Đồng năm 2023",
        },
        {
            id: "anh9",
            img: "../src/public/news/anh9.jpg",
            title: "Chú trọng học tập và làm theo Bác ở Trường Đại học Đà Lạt",
            date: "2023-04-24",
            view: "26",
            paragraph:
                "Là trường công lập đóng trên địa bàn tỉnh Lâm Đồng, Trường Đại học Đà Lạt (ĐHĐL) thực hiện nhiệm vụ chính trị, mục tiêu chung là đào tạo nhân lực, nâng cao dân trí, bồi dưỡng nhân tài; nghiên cứu khoa học, công nghệ tạo ra tri thức, sản phẩm mới, phục vụ yêu cầu phát triển kinh tế – xã hội, bảo đảm quốc phòng, an ninh và hội nhập quốc tế.",
        },
        {
            id: "anh10",
            img: "../src/public/news/anh10.jpg",
            title: "Trường Đại học Đà Lạt có 08 chương trình đào tạo đạt kiểm định chất lượng giáo dục",
            date: "2023-02-09",
            view: "163",
            paragraph:
                "Trường Đại học Đà Lạt tổ chức Lễ đón nhận Quyết định và Giấy chứng nhận kiểm định chất lượng chương trình đào tạo theo tiêu chuẩn của Bộ Giáo dục và Đào tạo cho 5 chương trình đào tạo và thông báo chính thức về 3 chương trình đào tạo khác của Trường đạt kiểm định chất lượng theo bộ tiêu chuẩn AUN-QA.",
        },
        {
            id: "anh11",
            img: "../src/public/news/anh11.jpg",
            title: "Tài liệu phục vụ Hội nghị khoa học “Khoa học và công nghệ phục vụ phát triển nông nghiệp công nghệ cao tại Lâm Đồng”",
            date: "2023-04-28",
            view: "35",
            paragraph: "Nội dung tài liệu",
        },
        {
            id: "anh12",
            img: "../src/public/news/anh12.jpg",
            title: "Tổ chức thành công Đại hội Công đoàn Trường Đại học Đà Lạt lần thứ XV",
            date: "2023-04-22",
            view: "32",
            paragraph:
                "Trong hai ngày 20-21/4, Công đoàn Trường Đại học Đà Lạt đã tổ chức thành công Đại hội lần thứ XV, nhiệm kỳ 2023-2028.",
        },
        {
            id: "anh13",
            img: "../src/public/news/anh13.jpg",
            title: "Kế hoạch phối hợp tổ chức lễ phát động “Tết trồng cây” trên địa bàn tỉnh Lâm Đồng năm 2023",
            date: "2023-05-16",
            view: "1",
            paragraph:
                "Kế hoạch số 639/KH-ĐHĐL ngày 16/5/2023 của Trường Đại học Đà Lạt.",
        },
        {
            id: "anh14",
            img: "../src/public/news/anh14.jpg",
            title: "Thông báo kết quả vòng 2 xét tiếp nhận và thay đổi chức danh nghề nghiệp viên chức năm 2023",
            date: "2023-04-28",
            view: "28",
            paragraph: "",
        },
        {
            id: "anh15",
            img: "../src/public/news/anh15.jpg",
            title: "Lan tỏa niềm yêu sách, khuyến khích văn hóa đọc trong học sinh, sinh viên Lâm Đồng",
            date: "2023-04-21",
            view: "20",
            paragraph:
                "Sáng 20-4, Sở Thông tin và Truyền thông tỉnh Lâm Đồng phối hợp Trường Đại học Đà Lạt tổ chức khai mạc Ngày Sách và Văn hóa đọc Việt Nam tỉnh Lâm Đồng lần thứ 2-năm 2023 và phát động phong trào xây dựng văn hóa đọc trên địa bàn tỉnh.",
        },
    ];
    const hotnewItems = [
        {
            id: 1,
            date: "2023-05-15",
            view: "125",
            label: "Tuyển sinh đại học 2023 – Những giấy tờ cần chuẩn bị",
        },
        {
            id: 2,
            date: "2023-05-15",
            view: " 21",
            label: "Khoa học và công nghệ phục vụ phát triển nông nghiệp công nghệ cao tại Lâm Đồng",
        },
        {
            id: 3,
            date: "2023-04-29",
            view: "39",
            label: "Trường Đại học Đà Lạt đạt nhiều thành tích tại Hội thao và Hội thi văn nghệ Khối thi đua các trường chuyên nghiệp – cao đẳng – đại học tỉnh Lâm Đồng năm 2023",
        },
    ];
    const notificationItems = [
        {
            id: 1,
            date: "2023-04-12",
            view: "46",
            label: "Thông báo về việc tổ chức bảo vệ luận án tiến sĩ cấp cơ sở – NCS Đàm Thị Thắm và NCS Lê Ngọc Bính – Chuyên ngành Văn học Việt Nam.",
        },
        {
            id: 2,
            date: "2023-04-06",
            view: "53",
            label: "Thông báo về việc tổ chức bảo vệ luận án tiến sĩ cấp cơ sở – NCS Trương Bá Phong – Chuyên ngành Sinh thái học",
        },
        {
            id: 3,
            date: "2023-04-05",
            view: "49",
            label: "Kế hoạch định kỳ chuyển đổi vị trí công tác đối với viên chức không giữ chức vụ lãnh đạo, quản lý năm 2023",
        },
        {
            id: 4,
            date: "2023-03-28",
            view: "56",
            label: "Thông báo tuyển sinh đi học tại Ca-dắc-xtan năm 2023",
        },
        {
            id: 5,
            date: "2023-03-16",
            view: "74",
            label: "Kế hoạch tổ chức tuyên truyền, vận động, sưu tầm, hiến tặng những hiện vật, tư liệu liên quan đến chặng đường 65 năm hình thành, đổi mới và phát triển của Trường Đại học Đà Lạt",
        },
    ];
    const meidaItems = [
        {
            id: "media1",
            pawth: "",
        },
    ];
</script>

<div class="main grid grid-cols-4 gap-4">
    <div class="news col-span-3">
        <h3><span class="span-h">Tin tức</span></h3>
        <div class="news-list grid grid-cols-3 grid-rows-5 gap-4">
            {#each newsItems as news}
                <div class="news-item col-span-1">
                    <img class="news-img" src={news.img} alt={news.id} />
                    <div class="news-container">
                        <a class="news-a" href="#">{news.title}</a>
                        <div class="news-time">
                            <span class="news-span">{news.date}</span>
                            <span class="news-span">{news.view}</span>
                        </div>
                        <p class="news-p">{news.paragraph}</p>
                    </div>
                </div>
            {/each}
        </div>
    </div>
    <div class="col-span-1 grid grid-cols-1">
        <div class="hot-news">
            <h3><span class="span-h">Tin nổi bật</span></h3>
            <div class="hotnews-list">
                {#each hotnewItems as item}
                    <div class="hotnews-item">
                        <div class="hotnews-index">{item.id}</div>
                        <div class="hotnews-content">
                            <div class="hotnews-meta">
                                <div class="hotnews-date">{item.date}</div>
                                <div class="hotnews-view">
                                    <svg
                                        width="14px"
                                        height="14px"
                                        viewBox="0 0 20 20"
                                        xmlns="http://www.w3.org/2000/svg"
                                        fill="none"
                                    >
                                        <path
                                            fill="#000000"
                                            fill-rule="evenodd"
                                            d="M3.415 10.242c-.067-.086-.13-.167-.186-.242a16.806 16.806 0 011.803-2.025C6.429 6.648 8.187 5.5 10 5.5c1.813 0 3.57 1.148 4.968 2.475A16.816 16.816 0 0116.771 10a16.9 16.9 0 01-1.803 2.025C13.57 13.352 11.813 14.5 10 14.5c-1.813 0-3.57-1.148-4.968-2.475a16.799 16.799 0 01-1.617-1.783zm15.423-.788L18 10l.838.546-.002.003-.003.004-.01.016-.037.054a17.123 17.123 0 01-.628.854 18.805 18.805 0 01-1.812 1.998C14.848 14.898 12.606 16.5 10 16.5s-4.848-1.602-6.346-3.025a18.806 18.806 0 01-2.44-2.852 6.01 6.01 0 01-.037-.054l-.01-.016-.003-.004-.001-.002c0-.001-.001-.001.837-.547l-.838-.546.002-.003.003-.004.01-.016a6.84 6.84 0 01.17-.245 18.804 18.804 0 012.308-2.66C5.151 5.1 7.394 3.499 10 3.499s4.848 1.602 6.346 3.025a18.803 18.803 0 012.44 2.852l.037.054.01.016.003.004.001.002zM18 10l.838-.546.355.546-.355.546L18 10zM1.162 9.454L2 10l-.838.546L.807 10l.355-.546zM9 10a1 1 0 112 0 1 1 0 01-2 0zm1-3a3 3 0 100 6 3 3 0 000-6z"
                                        />
                                    </svg>
                                    {item.view}
                                </div>
                            </div>
                            <div class="hotnews-lable">{item.label}</div>
                        </div>
                    </div>
                {/each}
            </div>
        </div>
        <div class="notification">
            <h3><span class="span-h">Thông báo</span></h3>
            <div class="notification-list">
                {#each notificationItems as item}
                    <div class="notification-item">
                        <div class="notification-index">{item.id}</div>
                        <div class="notification-content">
                            <div class="notification-meta">
                                <div class="notification-date">{item.date}</div>
                                <div class="notification-view">
                                    <svg
                                        width="14px"
                                        height="14px"
                                        viewBox="0 0 20 20"
                                        xmlns="http://www.w3.org/2000/svg"
                                        fill="none"
                                    >
                                        <path
                                            fill="#000000"
                                            fill-rule="evenodd"
                                            d="M3.415 10.242c-.067-.086-.13-.167-.186-.242a16.806 16.806 0 011.803-2.025C6.429 6.648 8.187 5.5 10 5.5c1.813 0 3.57 1.148 4.968 2.475A16.816 16.816 0 0116.771 10a16.9 16.9 0 01-1.803 2.025C13.57 13.352 11.813 14.5 10 14.5c-1.813 0-3.57-1.148-4.968-2.475a16.799 16.799 0 01-1.617-1.783zm15.423-.788L18 10l.838.546-.002.003-.003.004-.01.016-.037.054a17.123 17.123 0 01-.628.854 18.805 18.805 0 01-1.812 1.998C14.848 14.898 12.606 16.5 10 16.5s-4.848-1.602-6.346-3.025a18.806 18.806 0 01-2.44-2.852 6.01 6.01 0 01-.037-.054l-.01-.016-.003-.004-.001-.002c0-.001-.001-.001.837-.547l-.838-.546.002-.003.003-.004.01-.016a6.84 6.84 0 01.17-.245 18.804 18.804 0 012.308-2.66C5.151 5.1 7.394 3.499 10 3.499s4.848 1.602 6.346 3.025a18.803 18.803 0 012.44 2.852l.037.054.01.016.003.004.001.002zM18 10l.838-.546.355.546-.355.546L18 10zM1.162 9.454L2 10l-.838.546L.807 10l.355-.546zM9 10a1 1 0 112 0 1 1 0 01-2 0zm1-3a3 3 0 100 6 3 3 0 000-6z"
                                        />
                                    </svg>
                                    {item.view}
                                </div>
                            </div>
                            <div class="notification-lable">{item.label}</div>
                        </div>
                    </div>
                {/each}
            </div>
        </div>
        <div class="introduce col-span-1">
            <div><span class="span-h">Giới thiệu</span></div>
            <div class="introduce-items" />
        </div>
    </div>
</div>

<style>
    div {
        background-color: #fff;
    }
    .span-h {
        display: block;
        text-align: center;
        text-transform: uppercase;
        color: #5f7adb;
        font-size: 24px;
        font-weight: 700;
        line-height: 42px;
        margin: 20px 0;
    }
    .main {
        width: 1200px;
        max-width: 100%;
        margin: 0 auto;
    }
    .news-item {
        margin: 10px;
        width: 248px;
        height: 348px;
        overflow: hidden;
        margin: 0 auto;
        border-radius: 0 0 4px 4px;
        box-sizing: border-box;
        border: 1px solid #5f7adb;
    }
    .news-container {
        padding: 8px 8px 0px 8px;
    }
    .news-a {
        overflow: hidden;
        text-overflow: ellipsis;
        display: -webkit-box;
        -webkit-line-clamp: 2 !important;
        -webkit-box-orient: vertical;
        font-size: 16px;
        font-weight: 600;
    }
    .news-time {
    }
    .news-span {
        font-size: 10px;
        margin: 0 0 10px;
    }
    .news-p {
        font-size: 14px;
        text-overflow: ellipsis;
        display: -webkit-box;
        -webkit-line-clamp: 2 !important;
        -webkit-box-orient: vertical;
        overflow: hidden;
    }
    .hotnews-item {
        width: 362px;
        height: 98px;
        border: 1px solid #5f7adb;
        margin: 4px 0;
    }
    .hotnews-list {
    }
    .hotnews-item {
        display: flex;
        padding: 5px;
        overflow: hidden;
    }
    .hotnews-index {
        width: 70px;
        height: 64px;
        color: #5f7adb;
        font-size: 32px;
        font-weight: 700;
        margin: 0 10px;
        text-align: center;
    }
    .hotnews-content {
        width: 362px;
        height: 100px;
    }
    .hotnews-meta {
        display: flex;
        margin: 0 0 10px;
    }
    .hotnews-date {
        font-size: 14px;
        background-color: #fc7616;
        color: white;
        padding-left: 5px;
        padding-right: 5px;
    }
    .hotnews-view {
        font-size: 14px;
        margin: 0 10px;
        display: flex;
        align-items: center;
    }
    .hotnews-lable {
        font-size: 15px;
        display: -webkit-box;
        -webkit-line-clamp: 2 !important;
        -webkit-box-orient: vertical;
        overflow: hidden;
    }
    .notification {
    }
    .notification-item {
        width: 362px;
        height: 98px;
        border: 1px solid #5f7adb;
        margin: 4px 0;
    }
    .notification-list {
    }
    .notification-item {
        display: flex;
        padding: 5px;
        overflow: hidden;
    }
    .notification-index {
        width: 70px;
        height: 64px;
        color: #5f7adb;
        font-size: 32px;
        font-weight: 700;
        margin: 0 10px;
        text-align: center;
    }
    .notification-content {
        width: 362px;
        height: 100px;
    }
    .notification-meta {
        display: flex;
        margin: 0 0 10px;
    }
    .notification-date {
        font-size: 14px;
        background-color: #fc7616;
        color: white;
        padding-left: 5px;
        padding-right: 5px;
    }
    .notification-view {
        font-size: 14px;
        margin-left: 10px;
        display: flex;
        align-items: center;
    }
    .notification-lable {
        font-size: 15px;
        display: -webkit-box;
        -webkit-line-clamp: 2 !important;
        -webkit-box-orient: vertical;
        overflow: hidden;
    }
</style>
