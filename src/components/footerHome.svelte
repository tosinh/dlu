<script>
    import {
        Footer,
        FooterCopyright,
        FooterLinkGroup,
        FooterLink,
        FooterBrand,
        FooterIcon,
    } from "flowbite-svelte";
</script>

<Footer footerType="socialmedia">
    <hr class="my-6 border-gray-200 sm:mx-auto dark:border-gray-700 lg:my-8" />
    <div class="flex md:flex md:justify-around">
        <div class="mb-6 md:mb-0">
            <img
                href="https://www.google.com/maps/place/Tr%C6%B0%E1%BB%9Dng+%C4%90%E1%BA%A1i+H%E1%BB%8Dc+%C4%90%C3%A0+L%E1%BA%A1t/@11.9533848,108.4354931,15z/data=!4m6!3m5!1s0x317112d959f88991:0x9c66baf1767356fa!8m2!3d11.9545604!4d108.4442049!16s%2Fm%2F02rtwnx?entry=ttu"
                src="../src/public/home/map.png"
                alt="MapDLu"
                class="w-72"
            />
        </div>

        <div>
            <h2
                class="mb-6 text-sm font-semibold uppercase text-gray-900 dark:text-white"
            >
                TRƯỜNG ĐẠI HỌC ĐÀ LẠT
            </h2>
            <FooterLinkGroup>
                <div class="flex my-1.5">
                    <svg
                        version="1.1"
                        fill="#000"
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
                    <span class="mx-1.5"
                        >1 Phù Đổng Thiên Vương - P8 - TP.Đà Lạt</span
                    >
                </div>
                <div class="flex my-1.5">
                    <svg
                        fill="#000"
                        width="20px"
                        height="20px"
                        viewBox="0 0 32 32"
                        xmlns="http://www.w3.org/2000/svg"
                        ><path
                            d="M11.748 5.773S11.418 5 10.914 5c-.496 0-.754.229-.926.387S6.938 7.91 6.938 7.91s-.837.731-.773 2.106c.054 1.375.323 3.332 1.719 6.058 1.386 2.72 4.855 6.876 7.047 8.337 0 0 2.031 1.558 3.921 2.191.549.173 1.647.398 1.903.398.26 0 .719 0 1.246-.385.536-.389 3.543-2.807 3.543-2.807s.736-.665-.119-1.438c-.859-.773-3.467-2.492-4.025-2.944-.559-.459-1.355-.257-1.699.054-.343.313-.956.828-1.031.893-.112.086-.419.365-.763.226-.438-.173-2.234-1.148-3.899-3.426-1.655-2.276-1.837-3.02-2.084-3.824a.56.56 0 0 1 .225-.657c.248-.172 1.161-.933 1.161-.933s.591-.583.344-1.27-1.906-4.716-1.906-4.716z"
                        /></svg
                    >
                    <a class="mx-1.5" href="tel:0263 3822 246">0263 3822 246</a>
                    0263 3822 246 | Fax:
                    <a href="teL:0263.3823380">0263.3823380</a>
                </div>
                <div class="flex content-center my-1.5">
                    <svg
                        fill="#000"
                        width="20px"
                        height="20px"
                        viewBox="0 0 32 32"
                        xmlns="http://www.w3.org/2000/svg"
                        ><path
                            d="M5 24.225V7.776h22v16.447H5v.002zm3.011-1.815h15.978l-5.111-5.115L16 20.179l-2.877-2.883-5.112 5.114zm-1.216-1.275l5.077-5.09-5.077-5.065v10.155zm13.332-5.09l5.079 5.09V10.979l-5.079 5.066zm-4.126 1.588l8.022-8.027-16.045-.001 8.023 8.028z"
                        /></svg
                    >
                    <a class="mx-1.5" href="mailto:info@dlu.edu.vn"
                        >daihocdalat@dlu.edu.vn</a
                    >
                </div>
            </FooterLinkGroup>
        </div>
    </div>
    <hr class="my-6 border-gray-200 sm:mx-auto dark:border-gray-700 lg:my-8" />
    <div>
        <span>
            Copyright © 2020 Trung tâm Công nghệ Thông tin Trường Đại học Đà Lạt
        </span>
    </div>
</Footer>
