FROM redmine:alpine

RUN wget -O /usr/src/redmine/public/themes/yhtheme.zip https://github.com/yenihayat/redmine-theme-yh/archive/master.zip \ 
    && unzip /usr/src/redmine/public/themes/yhtheme.zip -d /usr/src/redmine/public/themes/ \
    && rm -f /usr/src/redmine/public/themes/yhtheme.zip

WORKDIR /usr/src/redmine/plugins

# redmine_recurring_tasks: 반복 작업을 위한 플러그인
# redmine_ckeditor: 위지윅 에디터
# redmine_startpage: 레드마인 사이트 접속 시 보여지는 첫 페이지를 변경해주는 플러그인
# redmine_lightbox2: 등록된 이미지, pdf 파일을 미리볼 수 있게 도와주는 플러그인
# redmine_banner: 공지사항을 배너 형식으로 표시
# sidebar_hide: Navbar를 숨길 수 있는 플러그인
# redmine_workflow_enhancements: 설정한 업무 흐름을 UI형식으로 시각화 하여 보다 쉽게 이해할수 있도록 표시해 주는 플러그인
# redmine_favourite_projects: 사용자가 톱 메뉴, 나의 페이지 or  Project Jumplist에 즐겨찾는 프로젝트 링크를  추가할수 있는 플러그인
# redmine_drawio: draw.io 레드마인 버전
# redmine_absolute_dates: 날짜를 절대값으로 바꾸는 플러그인
# redmine_percent_done: 완료 비율을 설정할 수 있는 플러그인
# redmine_issues_hub: 이슈를 모아볼 수 있는 플러그인
# redmine_issues_tree: redmine 공식 이슈 플러그인
# redmine_xlsx_format_issue_exporter: 이슈를 XLSX 형식 파일로 내보내는 Redmine 플러그인
RUN git clone --depth 1 https://github.com/centosadmin/redmine_recurring_tasks.git \
    && git clone --depth 1 https://github.com/a-ono/redmine_ckeditor.git \
    && git clone --depth 1 https://github.com/gatATAC/redmine_startpage.git \
    && git clone --depth 1 https://github.com/paginagmbh/redmine_lightbox2.git \
    && git clone --depth 1 https://github.com/akiko-pusu/redmine_banner.git \
    && git clone --depth 1 https://gitlab.com/bdemirkir/sidebar_hide.git \
    && git clone --depth 1 https://github.com/syntacticvexation/redmine_favourite_projects.git \
    && git clone --depth 1 https://github.com/mikitex70/redmine_drawio.git \
    && git clone --depth 1 https://github.com/suer/redmine_absolute_dates.git \
    && git clone --depth 1 https://github.com/jkraemer/redmine_percent_done.git \
    && git clone --depth 1 https://github.com/cappuMUC/redmine_issues_hub.git \
    && git clone --depth 1 https://github.com/Loriowar/redmine_issues_tree.git \
    && git clone --depth 1 https://github.com/two-pack/redmine_xlsx_format_issue_exporter.git \
    && git clone --depth 1 https://github.com/akiko-pusu/redmine_issue_templates.git

WORKDIR /usr/src/redmine

ENV RAILS_ENV="production"