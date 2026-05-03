<script setup lang="ts">
const publicConfig = useRuntimeConfig().public

const name = publicConfig.name || '123'
const phone = publicConfig.phone || '21235339'

useSeoMeta({
	title: `${name} - 自动化实习`,
	description: `${name}的自动化简历`,
	robots: 'noindex, nofollow',
})
</script>

<template>
<Builder class="block print:hidden" w="fit" m="is-auto x-1 y-.5" />
<article
	bg="white @dark:slate/10 print:transparent"
	p="6 print:x-2 print:y-0"
	text="3.7"
	tracking="wide"
	rounded="xl print:0"
>
	<h1 text="center" m="be-4">
		{{ name }}
	</h1>

	<ul columns="sm:2" p="is-0">
		<InfoLi icon="ri:smartphone-line" label="电话">
			{{ phone }} (同微信)
		</InfoLi>

		<InfoLi icon="ri:mail-line" label="邮箱">
			<InfoLink to="mailto:yxkswa@163.com" />
		</InfoLi>

		<!-- <InfoLi icon="ri:github-line" label="GitHub">
			<InfoLink to="https://github.com/L33Z22L11">
				L33Z22L11
			</InfoLink>
		</InfoLi> -->

		<InfoLi icon="ri:men-line" label="性别">
			男
		</InfoLi>

		<InfoLi icon="ri:school-line" label="学校">
			南京工业职业技术大学 (自动化技术与应用)
		</InfoLi>

		<InfoLi icon="ri:graduation-cap-line" label="学历">
			本科在读 (2027 届)
		</InfoLi>
	</ul>

	<InfoSection title="主修课程">
		<ul>
			<li>自动控制原理、PLC 编程、单片机原理、电气控制与变频技术、传感器与检测技术、工业机器人基础、EPLAN 电气制图、组态技术、电机与拖动、过程控制系统</li>
		</ul>
	</InfoSection>

	<InfoSection title="个人技能">
		<ul>
			<li>编程控制：西门子、PLC 编程；掌握单片机 C语言基础</li>
			<li>软件操作：会使用EPALN 绘制电气原理图、组态昆仑通态触摸屏组态、Office 办公套件</li>
			<li>硬件实操：理解低压电气接线、变频器、伺服电机、传感器安装调试、配电柜基础装配</li>
			<li>专业能力：初步了解自动化生产线流程、设备故障排查、简单工控系统调试、识图与图纸解读</li>
		</ul>
	</InfoSection>

	<!-- <InfoSection title="项目经验">
		<Project
			name="blog-v3"
			desc="个人博客"
			role="创建者"
			link="https://github.com/L33Z22L11/blog-v3"
			from="2024.08"
			:techs="['Nuxt', 'Vue 3', 'TypeScript', 'Pinia', 'Scss']"
		>
			<ul>
				<li>开源项目获 120+Stars，15+真实下游用户，通过 GitHub、交流群持续迭代项目，适配多个云构建平台的 SSR/SSG 功能。</li>
				<li>发现上游多处不合预期的问题，通过提交 Issue / PR、打 Patch 等方式修复。</li>
				<li>精校响应式设计、深色模式体验、文字排版布局，设计风格优雅统一，组件系统完善。</li>
				<li>通过 Google Search Console 监测发现境外繁体镜像站点，参阅 Whois、HTTP Header 等信息，定位到 Cloudflare 反代 + 域名替换的行为机制，开发出恶意反代跳转回原站的方案；同时排查 SEO 问题，优化至月 PV 10K。</li>
			</ul>
		</Project>

		<Project
			name="GioPic"
			desc="图床上传桌面程序"
			role="核心贡献者"
			link="https://github.com/isYangs/GioPic"
			from="2024.08"
			to="2025.02"
			:techs="['Electron', 'Vue 3', 'TypeScript', 'Axios', 'UnoCSS', 'NaiveUI']"
		>
			<ul>
				<li>解决跨平台启动问题，在 macOS 开发的项目在 Windows 上无法启动，通过查阅报错资料，修改构建脚本，实现多平台开发运行。</li>
				<li>提升项目扩展性，针对适配 AWS S3 / 第三方 OSS 存储源时代码扩展性差的问题，重构图床存储程序定义代码，实现第三方图床存储兼容。</li>
				<li>优化图标显示，针对 Windows 托盘图标、macOS 启动台图标比例异常问题，参考 Electron、Apple Developer 等文档规范，使用原型设计工具绘制图标并调整逻辑，实现多系统、多颜色模式下托盘、桌面图标完美显示。</li>
			</ul>
		</Project>
	</InfoSection> -->

	<InfoSection title="校园经历">
		<ul>
			<li>专业实训：参与自动化生产线组装与调试实训，负责电气接线、PLC 程序编写及设备联调，参与完成流水线启停、分拣控制功能</li>
			<li>课程设计：参与完成基于PLC的加料搅拌系统设计，参与完成方案设计、编程、接线及调试</li>
		</ul>
	</InfoSection>

	<InfoSection title="实习经历">
		<ul>
			<li>暂无实习经历</li>
		</ul>
	</InfoSection>

	<InfoSection title="个人证书">
		<ul>
			<li>英语四六级</li>
			<li>中国大学生计算机二级</li>
		</ul>
	</InfoSection>
</article>
</template>
